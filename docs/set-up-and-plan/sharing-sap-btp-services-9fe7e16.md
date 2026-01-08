<!-- loio9fe7e160bf58488aa42e726ebe3c7111 -->

# Sharing SAP BTP Services

Some SAP BTP services can be shared across subaccounts for cost-efficiency and centralized governance, with options for instance sharing or centralized setups depending on the service. Using shared SAP BTP services can streamline administration and facilitate role management.



<a name="loio9fe7e160bf58488aa42e726ebe3c7111__section_qwx_1q3_q2c"/>

## Overview

In general, there are two ways of sharing SAP BTP services:

-   There are various SAP BTP services you can set up as shared services, often across landscapes. For example, you might use them to manage data flows within a landscape. You simply create an instance of these services in a central subaccount, and then directly use it in other subaccounts to integrate them into your projects, eliminating the need for instance sharing.

    For some services, it's recommended to set up more than one central instance, so that you can test changes in DEV/TEST/PROD instances. For other services, using one instance is sufficient.

-   For SAP BTP services that support **instance sharing**, you set up a central instance and then configure your project-related subaccounts to access the central service instance. This setup mimics the instance running locally within the same subaccount but without consuming additional quota as if it's running locally.

    The way to set up instance sharing depends on the individual service. Check out the service documentation for specific instructions.

    > ### Tip:  
    > If you prefer working with CLI, see [btp share services/instance](https://help.sap.com/docs/btp/btp-cli-command-reference/btp-share-services-instance).




<a name="loio9fe7e160bf58488aa42e726ebe3c7111__section_dls_fq3_q2c"/>

## Set Up as a Shared Service

See the following examples for services that might qualify to be run centrally as shared services:



### Without Instance Sharing

-   [SAP Automation Pilot](https://help.sap.com/docs/automation-pilot?locale=en-US) is designed as a centralized service. Set up one instance.

-   [SAP Build Work Zone](https://help.sap.com/docs/build-work-zone-standard-edition?locale=en-US): Depending on your requirements, SAP Build Work Zone can either be set up as a central shared service \(to allow your end users access from a central place, optionally complemented with the concept of “sites” to cater to different use cases served from central instances\) - or in a distributed/mixed way, where you create dedicated/additional instances of SAP Build Work Zone in non-central/non-shared subaccounts. Applying a standard staged setup is recommended in either case.

-   [SAP Business Application Studio](https://help.sap.com/docs/bas?locale=en-US): For a limited number of apps or developers, set up one instance.

-   [SAP Cloud Logging](https://help.sap.com/docs/cloud-logging?locale=en-US): You can share one instance between different subaccounts, Cloud Foundry spaces, or Kyma clusters.

-   [SAP Cloud Transport Management](https://help.sap.com/docs/cloud-transport-management?locale=en-US) \(cTMS\) is designed as a centralized service.

    To facilitate role management and configure strict access control, set up one or more instances: cTMS needs destinations within a subaccount that point to PROD accounts. If you set up cTMS in a DEV subaccount, all DEV admins can also access PROD destinations, which you might want to prevent. Furthermore, you need separate instances for isolation between the transport landscapes of different teams. Lastly, if you exceed the storage capacity \(see [Background Information: Storage Capacity](https://help.sap.com/docs/cloud-transport-management/sap-cloud-transport-management/background-information-storage-capacity?locale=en-US)\), you need more than one instance.

-   [SAP Integration Suite](https://help.sap.com/docs/integration-suite?locale=en-US): To develop and change iFlows, set up two or more instances. For details, see [Considerations on the System Landscape for Integration when On-boarding into SAP Cloud Integration](https://blogs.sap.com/2019/05/21/considerations-on-the-system-landscape-for-integration-when-on-boarding-into-sap-cloud-platform-integration-for-process-services/).

-   [SAP Task Center](https://help.sap.com/docs/task-center?locale=en-US)




### With Instance Sharing

-   [SAP Credential Store](https://help.sap.com/docs/credential-store?locale=en-US): For details, see [Share, Unshare, and Authorize a Service Instance](https://help.sap.com/docs/credential-store/sap-credential-store/share-unshare-and-authorize-service-instance?locale=en-US).

-   [SAP HANA Cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/map-sap-hana-database-to-another-environment-context): Set up two or more instances. For details, see [Subscribing to the SAP HANA Cloud Administration Tools \(Multi-Environment\)](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/subscribing-to-sap-hana-cloud-administration-tools), [Map an SAP HANA Database to Another Environment Context](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/map-sap-hana-database-to-another-environment-context), and [Accessing SAP HANA Cloud](https://discovery-center.cloud.sap/card/239bed63-a3b0-44bd-86d6-00d07d948844).

-   [Object Store on SAP BTP](https://help.sap.com/docs/object-store?locale=en-US): For details, see [Instance Sharing](https://help.sap.com/docs/object-store/object-store-service-on-sap-btp/instance-sharing-capability?locale=en-US).

-   [PostgreSQL on SAP BTP](https://help.sap.com/docs/postgresql-hyperscaler-option?locale=en-US): For details, see [Instance Sharing](https://help.sap.com/docs/postgresql-hyperscaler-option/postgresql-on-sap-btp-hyperscaler-option/instance-sharing?locale=en-US).

-   [Redis on SAP BTP](https://help.sap.com/docs/redis-hyperscaler-option?locale=en-US): For details, see [Instance Sharing](https://help.sap.com/docs/redis-hyperscaler-option/redis-on-sap-btp-hyperscaler-option/instance-sharing?locale=en-US).


> ### Tip:  
> For guidance about sharing SAP BTP, Kyma runtime instances, see [Sharing Clusters in Kyma](sharing-clusters-in-kyma-57ec1ea.md).



<a name="loio9fe7e160bf58488aa42e726ebe3c7111__section_btx_zty_r2c"/>

## Don’t Set Up as a Shared Service

See the following examples for services that cannot or should not run centrally:

-   [SAP Alert Notification service for SAP BTP](https://help.sap.com/docs/alert-notification?locale=en-US) instances must be set up at Cloud Foundry space level.

-   [SAP Content Agent service](https://help.sap.com/docs/content-agent-service?locale=en-US) instances must be set up on subaccount level, because the service acts as a local agent.

-   [SAP Continuous Integration and Delivery](https://help.sap.com/docs/continuous-integration-and-delivery?locale=en-US) should run on a team subaccount to keep the number of admins low and in context, because all admins can use all credentials stored inside a service instance.

-   [SAP Job Scheduling service](https://help.sap.com/docs/job-scheduling?locale=en-US) should be set up at Cloud Foundry space level.

-   [SAP Mobile Services](https://help.sap.com/docs/mobile-services?locale=en-US)


**Related Information**  


[Sharing Instances](https://help.sap.com/viewer/09cc82baadc542a688176dce601398de/Cloud/en-US/96d39daca76540e194688fd0b3f11396.html "Share service instances across applications within the same subaccount using SAP Service Manager to streamline data exchange, reduce costs, and simplify resource management.") :arrow_upper_right:

[Sharing Databases with Other Subaccounts](https://help.sap.com/viewer/3fa880aa54b74110ae99ad01503fcd60/Cloud/en-US/322080db84734e9b8812ede13703b83c.html "You can share a SAP ASE database that is owned by a subaccount with other subaccounts in the Neo environment.") :arrow_upper_right:

[Sharing Databases in the Same Global Account](https://help.sap.com/viewer/3fa880aa54b74110ae99ad01503fcd60/Cloud/en-US/1cc5e1efb7f640329f419b53f21c0906.html "You can share SAP ASE databases that have been provisioned in a subaccount with other subaccounts of your global account in the Neo environment.") :arrow_upper_right:

[Map an SAP HANA Database to Another Environment Context](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/map-sap-hana-database-to-another-environment-context)

[Cloud Foundry: Sharing service instances](https://docs.cloudfoundry.org/devguide/services/sharing-instances.html)

[SAP Cloud Logging: Share Service Instance Across Different Spaces](https://help.sap.com/docs/cloud-logging/cloud-logging/ingest-via-cloud-foundry-runtime?locale=en-US&version=Cloud#loiof5a7c993743c4ee79722479371b90b37__share_service_instance_across_different_spaces)

