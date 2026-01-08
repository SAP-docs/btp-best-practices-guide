<!-- loio898509dd6f1346448d5057f4dc6b8b30 -->

# Shared Responsibility Model Between You and SAP

A shared responsibility model applies to SAP BTP: SAP manages the platform, while you develop and manage your applications, data, content, and integrations. The infrastructure provider is responsible for managing the underlying infrastructure and the data center.



> ### Caution:  
> This shared responsibility model is specific to SAP BTP, Multi-Cloud Foundation. While many principles also apply to SAP BTP, Neo, some details may differ and you should evaluate them on a case-by-case basis.

![](images/sap_cp_lm_shared_responsibility_model_e94f81a.png)



<a name="loio898509dd6f1346448d5057f4dc6b8b30__section_customer_responsibilities"/>

## Your Responsibilities

As an SAP BTP customer, you’re responsible for the following areas:

-   Change Management and Operations

    You establish and run effective change management processes for your applications and integrations. If you use open-source software, you must keep it updated and include vulnerability scanning in your development process.

-   Customer Data and Content

    You are responsible for your data and content, which includes ensuring data privacy.

-   Application Development and Integration

    You develop and operate your applications on SAP BTP. This includes creating, deploying, and integrating them with other systems.

-   Account and Environment Management

    You manage your account structure, which includes organizing directories, subaccounts, and service instances. You define an account strategy based on your organization's requirements, create and configure subaccounts for your development projects, and allocate resources and services as needed. For a more detailed breakdown of responsibilities, see [Operating Model](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/9aafc94077c0447c88e2f5f2024a9c8e.html "An operating model clearly defines the separation of tasks between SAP and the customer during all phases of an integration project.") :arrow_upper_right:.

-   Authorization and Identity Management

    You manage users and assign authorizations according to your organizational and project needs. To meet these needs, use the authorization and identity management tools that SAP provides.




<a name="loio898509dd6f1346448d5057f4dc6b8b30__section_pgq_vlf_ngc"/>

## Joint Responsibilities

You and SAP share responsibility for the following key areas:

-   Observability

    SAP oversees monitoring for all SAP BTP services. This includes performing health checks, troubleshooting, housekeeping tasks, and incident management to provide a reliable and resilient platform-as-a-service environment.

    Use SAP BTP's monitoring features and add your own monitoring or health checks as needed. Regularly perform housekeeping and troubleshoot issues related to your components. If an issue is SAP's responsibility, create an incident and follow the SAP support process.

-   Security and Compliance

    SAP prioritizes your data security and compliance. We follow strict standards to protect your data and meet regulatory requirements. Our security measures meet industry standards for cybersecurity, operations, and privacy. SAP manages security and compliance risks through cybersecurity and physical security programs that cover our cloud environments, facilities, events, and employees. For more information on SAP's security policies or to access compliance documentation, visit the [SAP Trust Center](https://www.sap.com/about/trust-center.html).

    You are also responsible for the security and compliance of your solutions. We recommend that you follow the security recommendations for applications built on SAP BTP \(see [SAP BTP Security Recommendations](https://help.sap.com/docs/btp/sap-btp-security-recommendations-c8a9bb59fe624f0981efa0eff2497d7d/sap-btp-security-recommendations?version=Cloud)\).

-   High Availability and Disaster Recovery

    For all SAP-managed services running on SAP BTP, SAP guarantees deployment according to strict service-level agreements \(SLAs\) to ensure high availability, stability, and smooth operations. In the event of a disaster, SAP maintains regular backups and offers disaster recovery mechanisms. For details, see [Resilience, High Availability, and Disaster Recovery](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e3ac4f7c25a3442ca585950095eec599.html#loioe3ac4f7c25a3442ca585950095eec599 "SAP has a number of processes in place to support resilience in SAP BTP, and provides different offerings so that you can support the high availability of your applications.") :arrow_upper_right:.

    While SAP provides most high availability \(HA\) and disaster recovery \(DR\) features by default, you also have specific responsibilities. For example, when you deploy custom applications and extensions in SAP BTP, you must ensure that they run with at least three instances \(where applicable\). Additionally, configure SAP HANA Cloud with replicas for better resilience. These actions are essential to ensure that the high availability and disaster recovery concepts function as intended. For further details, see [Resilience, High Availability, and Disaster Recovery](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e3ac4f7c25a3442ca585950095eec599.html#loioe3ac4f7c25a3442ca585950095eec599 "SAP has a number of processes in place to support resilience in SAP BTP, and provides different offerings so that you can support the high availability of your applications.") :arrow_upper_right:.




<a name="loio898509dd6f1346448d5057f4dc6b8b30__section_sap_responsibilities"/>

## SAP's Responsibilities

As the service provider, SAP is responsible for the following areas:

-   Global Accounts and Entitlements Provisioning

    SAP creates your global account and assigns the necessary entitlements so you can start using SAP BTP. During this provisioning process, SAP grants initial global account administrator rights to your designated administrator.

-   Runtimes and Services Management

    SAP delivers and operates the services and runtimes of SAP BTP, including solutions such as Cloud Foundry, SAP Integration Suite, SAP Build, and more. SAP also implements regular updates to ensure that these services remain current and secure.

    When you use the SAP BTP, Kyma runtime, you have full access to your cluster, except for the `kyma-system` namespace. SAP exclusively manages and monitors this namespace to ensure stability and security. For the SAP BTP ABAP environment, you can manage certain aspects through the Landscape Portal.




<a name="loio898509dd6f1346448d5057f4dc6b8b30__section_infrastructure_provider_responsibilities"/>

## Infrastructure Provider's Responsibilities

The infrastructure level is managed by either SAP or a hyperscaler, with SAP overseeing the relationship with hyperscalers. Even when using hyperscaler regions, SAP is responsible for managing this relationship. As a customer using SAP BTP, you don't have to interact directly with the hyperscalers.

The infrastructure providers operate the physical data centers that host SAP BTP regions. Their responsibilities include:

-   Set up and maintain the data centers, including servers, networking, and power supply.

-   Ensure physical and digital security to prevent unauthorized access.

-   Meet industry-grade standards for reliability and compliance.

-   Manage infrastructure operations, including software updates and patches.


