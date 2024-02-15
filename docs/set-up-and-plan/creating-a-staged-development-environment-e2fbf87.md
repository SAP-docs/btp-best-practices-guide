<!-- loioe2fbf8789bd64683904083ca89350db6 -->

# Creating a Staged Development Environment

The number of subaccounts and directories you create, and for which purpose, depends on your organizational setup and your use case.

We generally recommend using subaccounts for a staged development process, where you separate between a subaccount for development, one for testing, and one for production:

-   Development – for development purposes and for testing individual increments in the cloud.
-   Testing – for integration testing and testing in production-like environment before making it publicly available, to ensure quality delivery. In highly DevOps-driven companies, this subaccount is also used for production applications, as testing occurs in the development subaccount.
-   Production – for production applications.

![](images/sap_cp_lm_account_model_scenarios_1_e6e2d62.png)

Other typical reasons for creating subaccounts include the following:

-   Separate development scenarios and projects for easier configuration, for example, with regard to access restrictions.

-   Separate the work of different development teams.

-   Restrict access to applications and their administration, for example, by setting up "high-security" subaccounts with restricted access, or creating separate subaccounts to connect with your different back-end systems.

-   Share an SAP HANA Cloud database in one subaccount with similar projects managed in other subaccounts.

Keep in mind the following considerations when creating different subaccounts:

-   Connections to on-premise systems must be made separately for each subaccount, which also means more work for your Platform Engineering Team. However, it might be easier for you to shut down all integration paths for a project if you've maintained them all in one subaccount. This also lets you control which application uses which on-premise connections.
-   When choosing a region for your subaccount, consider that the region should be close to your customers' geographic location to reduce network latency. In extension scenarios, choose a region that's close to the systems involved. Also, consider any legal requirements and the load distribution when choosing a region.

-   If your S/4HANA tenants must be segregated for legal or regulatory reasons \(for example, for the segregation of subsidiaries of a company\), use different subaccounts for their extensions.

-   If the DevOps or operations teams for applications within one subaccount are completely separate, consider creating separate subaccounts for them for better maintainability.


> ### Recommendation:  
> We recommend building an account structure that can easily scale once your organization gets larger or more projects are added. In other words, you may want to start off with just subaccounts and add directories for grouping these subaccounts as the need arises.



<a name="loioe2fbf8789bd64683904083ca89350db6__section_t4w_bxq_k2b"/>

## Example Account Models

Consider the following account scenarios for creating your own account model:

-   [Account Model with Subaccounts](account-model-with-subaccounts-049d331.md)
-   [Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd)

