<!-- loio4cb5276d832847aa8e5c82e73ef9ff10 -->

# Subaccounts or Spaces/Namespaces?

Within subaccounts, you can further break down your account model: In a Cloud Foundry org, you create “spaces”; in a Kyma cluster, you create “namespaces”. You can use both, subaccounts and spaces/namespaces, to develop applications and to use services and functions.



<a name="loio4cb5276d832847aa8e5c82e73ef9ff10__section_ftm_rpx_c2c"/>

## Overview

Generally speaking, subaccounts are for isolation, while spaces and namespaces are for structuring.

Whether you want to use subaccounts or spaces/namespaces depends a lot on your preference - customers have set up many successful account models either way. However, some features are only available for subaccounts or spaces or namespaces, which may influence your decision.

> ### Recommendation:  
> At the very least, we recommend that you create two different subaccounts for a staged development environment \(see [The Basic Account Model](setting-up-your-account-model-2db81f4.md#loio2db81f42f5194454beecde6cd4994dda__section_basic_account_model)\). This way, you can have dedicated user management between the different stages, as well as dedicated data management in elastic services, such as SAP HANA Cloud. Within each subaccount \(that is, Cloud Foundry org and Kyma cluster\), you can then create dedicated spaces/namespaces for each application, extension, solution, team, or other project.
> 
> If you have dependencies to SAP BTP services that don't support the concept of spaces or namespaces, use subaccounts.

When you decide whether to create different subaccounts or spaces/namespaces within one subaccount, consider the different features:

**Features in Subaccounts, Spaces, and Namespaces**


<table>
<tr>
<th valign="top">

Feature

</th>
<th valign="top">

Subaccount

</th>
<th valign="top">

Cloud Foundry Space

</th>
<th valign="top">

Kyma Namespace

</th>
</tr>
<tr>
<td valign="top">

Segregation for data access, data visibility, network connectivity, and ingress traffic

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Dedicated data management in elastic services, such as SAP HANA Cloud

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Configure trust for user management

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Grant access privileges and authorizations

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

Integration options \(destinations, formations, Cloud Connector\)

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Monitor cost and usage in SAP BTP cockpit or with public APIs

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Limit resource usage

</td>
<td valign="top">

Yes \(mandatory\)

</td>
<td valign="top">

No SAP BTP quotas, but space quotas.

</td>
<td valign="top">

No, but you can set limits for resource consumption on namespace level.

</td>
</tr>
</table>



<a name="loio4cb5276d832847aa8e5c82e73ef9ff10__section_segregation"/>

## Segregation

-   In regard to tenant isolation, think of a subaccount as a tenant: Segregation for data access, data visibility, network connectivity, and ingress traffic happens on subaccount level, not on the level of applications or Cloud Foundry spaces/Kyma namespaces.

-   You can configure your own group of business users for subaccounts, as well as for Kyma namespaces, but not for Cloud Foundry spaces.

-   You can set up roles and trust for subaccounts and Kyma namespaces. For Cloud Foundry, you can assign Cloud Foundry roles at the org and space level.

-   Identity providers are assigned on global account, directory, subaccount, and runtime level, but not on the level of Kyma namespaces or Cloud Foundry spaces.

-   Integration options \(such as destinations, formations, and Cloud Connector\) are supported on subaccount level, but not for spaces or namespaces.

    To connect a DEV subaccount with a DEV on-premise system; and a PROD subaccount with a PROD on-premise system, set up dedicated cloud connector tunnels. For details, see [Document the Landscape of a Hybrid Solution](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/process-guidelines-for-hybrid-scenarios?version=Cloud#document-the-landscape-of-a-hybrid-solution).


> ### Tip:  
> In SAP BTP, Kyma runtime, we recommend mounting the Secret of the service binding as a volume. When using the service binding mechanism with volume mounts, applications can consume services only within their own namespace.



<a name="loio4cb5276d832847aa8e5c82e73ef9ff10__section_billing"/>

## Billing

-   You can **monitor** the consumption of resources in your global account only per directory or subaccount \(Cloud Foundry org/Kyma cluster\) and space, not per application or Kyma namespace. To monitor the resources consumed by a specific project, department, or application, create a dedicated subaccount for them.

-   Accurate **billing** is only possible for global accounts. For the consumption-based model, you can calculate costs according to usage, but note that this is only approximate. See [Monitoring Usage and Consumption Costs in Your Global Account](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/de6f0db8919f4e6f97e54bc4ddaf2ab8.html "SAP BTP cockpit supports advanced usage and cost monitoring of services in your global account. You can compare the usage and costs of multiple services and subaccounts, see monthly trends, and drill down into subaccounts and service plans for detailed information.") :arrow_upper_right: and [Managing Cost](managing-cost-c615301.md).

-   You can assign SAP BTP **quotas** to subaccounts, see [Entitlements and Quotas](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/00aa2c23479d42568b18882b1ca90d79.html "When you purchase an enterprise account, you’re entitled to use a specific set of resources, such as the amount of memory that can be allocated to your applications.") :arrow_upper_right:. If you're using one of the SAP BTP services that don't support fixed quotas, make sure to monitor usage and cost.

    In Cloud Foundry spaces, you can create space quotas - see [Create Space Quotas](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/b13c4a2666dd4018a52780da581bbf6d.html "You can use the SAP BTP cockpit to create space quotas.") :arrow_upper_right:, which are slightly different. In Kyma namespaces, you can set limits for resource consumption on namespace level with [Kubernetes quotas](https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/quota-memory-cpu-namespace/).


> ### Tip:  
> Provisioning a Kyma cluster isn't free of cost. Use subaccounts only if you need them for segregation, not just for structuring purposes. For details, see [Sharing Clusters in Kyma](sharing-clusters-in-kyma-57ec1ea.md).

**Related Information**  


[Configuring a Custom Identity Provider for Kyma](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/67bcc6e2d4d749659faf3ede1853f19e.html "Enable the Kyma environment with a custom identity provider (IdP).") :arrow_upper_right:

[Role-Based Access Control \(RBAC\) in Kyma](role-based-access-control-rbac-in-kyma-bb31080.md "Assigning permissions in Kyma is based on the Kubernetes role-based access control (RBAC). It’s recommended that you start with separating the developers and operators of a cluster. Later, you can refine the role concept as required.")

