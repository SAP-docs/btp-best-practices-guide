<!-- loio2c30208f5bfd4608a19fc5d5e964e5ec -->

# Setting Up Identity Lifecycle

As people join, change roles, and eventually leave your organization, you care for the onboarding, maintenance, and offboarding of their users in your systems. If you're a small organization, you can use manual processes, otherwise you need to automate.

We recommend creating users within the SAP Cloud Identity Services. The persistency layer of SAP Cloud Identity Services is the Identity Directory. Use SAP Cloud Identity Services - Identity Provisioning to provision users to SAP cloud solutions, such as SAP BTP. Identity Provisioning has connectors to distribute user artifacts needed at different levels of your SAP BTP accounts. By managing your identities centrally, you also ensure that when you offboard users, they're removed from target systems.

The global user ID is a unique identifier across technology layers, products, and solutions in the Intelligent Enterprise. The global user ID enables you to correlate information about a user across applications. SAP Cloud Identity Services is best equipped to handle SAP-specific attributes, such as the global user ID. In fact, some services and solution only function when using SAP Cloud Identity Services to manage the global user ID. SAP Cloud Identity Services can generate the global user ID or you must fill it yourself.

> ### Recommendation:  
> If you generate your own global user ID, don't use attributes such as an e-mail address. E-mail addresses are often based on a person's name. Names change, for example when a person changes their marital status or for other reasons. We generate a universally unique identifier \(UUID\) that remains stable as long as the user is in the system.
> 
> For more information, see [Global User ID in Integration Scenarios](https://help.sap.com/docs/SAP_CLOUD_IDENTITY/b95c3d5bab324a3a8409eee5267a5b75/a04611df60404a248a7a8089c85b9761.html) in the *System Integration Guide for SAP Cloud Identity Services*.

  
  
**SAP Cloud Identity Services Managing SAP Cloud Applications**

![](images/Identity_Lifecycle_04a07c3.png "SAP Cloud Identity Services Managing SAP Cloud Applications")

If you already have your own identity and access management solution, use this solution to ensure the correctness and consistency of user data. Identity Provisioning synchronizes the user or group data between SAP Cloud Identity Services and all SAP cloud applications, eliminating the need to maintain custom point-to-point connections.

For more information, see *System Integration Guide for SAP Cloud Identity Services*:

-   [Scenario Recommendations](https://help.sap.com/docs/SAP_CLOUD_IDENTITY/b95c3d5bab324a3a8409eee5267a5b75/9fc378782ba14f2b8ed1cf2f05c45405.html)

-   [SAP BTP Integration Scenario](https://help.sap.com/docs/SAP_CLOUD_IDENTITY/b95c3d5bab324a3a8409eee5267a5b75/0c3b5dc775794703b57ed7b01f679e45.html)


To authenticate with SAP BTP, the system needs user artifacts such as:

-   E-mail address of the user

-   Identity provider that authenticates the user


The ABAP and Kyma environments require a unique email address.

An administrator can create these users manually or in some cases allow for automatic creation after successful authentication at the identity provider. SAP BTP provides tools such as the SAP BTP cockpit, command-line interfaces, and APIs to enable you to manage this data yourself.

**Related Information**  


[Account Administration](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/5d62ec89de39442f8f31d527855cbced.html)

[Complying with Data Protection and Privacy Requirements](complying-with-data-protection-and-privacy-requirements-84e144a.md "All companies must respect data protection and privacy rights of individuals. Data protection and privacy most likely influences the architecture and functionalities of your application and should be considered as early as possible in the development process.")

