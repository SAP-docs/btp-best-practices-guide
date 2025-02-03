<!-- loioe2fbf8789bd64683904083ca89350db6 -->

# Creating a Staged Development Environment

When you're setting up a staged development environment, you must decide how many subaccounts you create, and for which purpose. Depending on your use case and your organizational setup, consider also using directories and other structuring elements.

> ### Recommendation:  
> We recommend building an account structure that can easily scale once your organization gets larger or more projects are added. In other words, you may want to start off with just subaccounts and add directories for grouping these subaccounts as the need arises.
> 
> Evaluate which setup is best for your specifc organization. For example, to structure your account model for accounting purposes, consider separation by directories, subaccounts, or even global accounts.



<a name="loioe2fbf8789bd64683904083ca89350db6__section_hr1_psk_31c"/>

## Subaccounts for Staged Development

It's common to use subaccounts for a staged development process, where you separate between subaccounts for development, testing, and production. A typical setup consists of three subaccounts. However, you can choose to handle development and testing in the same subaccount; or if you want to reflect a larger backend landscape, use more than three subaccounts.

![](images/sap_cp_lm_account_model_scenarios_1_e6e2d62.png)

-   Development – for development purposes and for testing individual increments in the cloud.
-   Testing – for integration testing and testing in production-like environment before making it publicly available, to ensure quality delivery. In highly DevOps-driven companies, this subaccount is also used for production applications, as testing occurs in the development subaccount.
-   Production – for production applications.

> ### Example:  
> You are currently using Cloud Foundry and would like to start using Kyma as well – to use new services, or to migrate some services from Cloud Foundry to Kyma. Such approaches always require finding a balance between flexibility and costs.
> 
> In some cases, using the same subaccount for Cloud Foundry and Kyma for the same landscape makes sense: This way, you can reuse or share some SAP BTP services, for example, SAP HANA Cloud. In this example, one recommendation could be having the same **Prod** subaccount for both Cloud Foundry and Kyma. But for **Dev** and **Test**, you might choose to create separate subaccounts. For details, see [Staged Development with the Kyma Environment](staged-development-with-the-kyma-environment-ec8a269.md).
> 
> However, if your existing subaccount landscape is more complex and you have several teams, each with multiple subaccounts, then it's recommended to create specific subaccount for SAP BTP, Kyma runtime, to which the teams get access. Instead of subaccounts, use namespaces for isolation - for details, see [Sharing Clusters in Kyma](sharing-clusters-in-kyma-57ec1ea.md).



<a name="loioe2fbf8789bd64683904083ca89350db6__section_z4c_qsk_31c"/>

## Subaccounts for Other Purposes

Other typical reasons for creating subaccounts include the following:

-   Separate development scenarios and projects for easier configuration, for example, with regard to access restrictions.

-   Separate the work of different development teams.

-   Restrict access to applications and their administration, for example, by setting up "high-security" subaccounts with restricted access, or creating separate subaccounts to connect with your different back-end systems.

-   Share an SAP HANA Cloud database in one subaccount with similar projects managed in other subaccounts.

-   Use dedicated \(central\) subaccounts for shared services such as SAP Integration Suite, SAP Build Work Zone or Task Center, which by nature integrate with different applications running in separate \(local\) subaccounts.


Keep in mind the following considerations when creating different subaccounts:

-   Connections to on-premise systems must be made separately for each subaccount, which also means more work for your Platform Engineering Team. However, it might be easier for you to shut down all integration paths for a project if you've maintained them all in one subaccount. This also lets you control which application uses which on-premise connections.

-   When choosing a region for your subaccount, consider that the region should be close to your customers' geographic location to reduce network latency. In extension scenarios, choose a region that's close to the systems involved. Also, consider any legal requirements and the load distribution when choosing a region.

-   If your SAP S/4HANA tenants must be segregated for legal or regulatory reasons \(for example, for the segregation of subsidiaries of a company\), use different subaccounts for their extensions.

-   If the DevOps or operations teams for applications within one subaccount are completely separate, consider creating separate subaccounts for them for better maintainability.




<a name="loioe2fbf8789bd64683904083ca89350db6__section_t4w_bxq_k2b"/>

## Example Account Models

Consider the following account scenarios for creating your own account model:

-   [Account Model with Subaccounts](account-model-with-subaccounts-049d331.md)
-   [Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd)

