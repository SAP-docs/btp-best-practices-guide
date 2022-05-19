<!-- loio2db81f42f5194454beecde6cd4994dda -->

# Setting Up Your Account Model

The hierarchical structure between global accounts, directories, and subaccounts lets you define an account model that accurately fits your business and development needs.

Once you've signed your commercial contract with SAP, you'll receive access information and credentials for your global account. Use this account to manage the resources and entitlements for your development projects; it's the realization of your commercial contract with SAP. You'll also receive a bill for all resources used in your global account. If you require multiple global accounts for compliance or other reasons, you'll need to sign a dedicated contract for each one.

> ### Note:  
> SAP is currently migrating all global accounts from cloud management tools feature set A to the renovated cloud management tools feature set B. We’re doing this migration as a phased rollout, which is why cloud management tools feature sets A and B currently coexist. One big change that came with feature set B is a renovated account model: With feature set B, you can use**directories** to group and manage subaccounts inside your global account. For more information, see [Cloud Management Tools - Feature Set Overview](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/caf4e4e23aef4666ad8f125af393dfb2.html). Please make sure to understand if your global account is already on feature set B.

Within a global account that is on feature set B, you can create up to five levels of directories to further structure your global account according to your business or technical needs. To actually develop and deploy applications, to use services, and to subscribe to business applications provided by SAP, you need to create subaccounts. Directories are optional, but highly recommended as they offer a way to organize your subaccounts and to manage entitlements or users for an entire group of subaccounts. This means you can distribute the resources that are assigned to your global account across directories, and from there to the subaccounts inside a directory. Directories and subaccounts let you structure a global account according to the requirements of your organization and projects with regards to users, authorizations, and quotas.



<a name="loio2db81f42f5194454beecde6cd4994dda__section_rwt_5sr_fnb"/>

## Tools For Account Administration

The most important step in account model setup is to work out a concept that meets your business and technical requirements. The account models in this guide are designed to help you accomplish this. However, when it comes to acctually creating directories and subaccounts in your global account, you can choose between different experiences:

-   [Account Administration in the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8061ecc529d74465b2b9566a634943ec.html "Learn about frequent administrative tasks you can perform using the SAP BTP cockpit, such as managing global accounts, directories, subaccounts, entitlements, and members.") :arrow_upper_right:

-   [Account Administration Using the SAP BTP Command Line Interface (btp CLI) [Feature Set B]](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/7c6df2db6332419ea7a862191525377c.html "Use the SAP BTP command line interface (btp CLI) for account management tasks, such as creating or updating subaccounts and directories, and managing entitlements. It is a an alternative to the SAP BTP cockpit for all users who like to work in a terminal or want to automate operations using scripts.") :arrow_upper_right:

-   [Account Administration Using APIs](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1c8db1483d914cd99047aac5280f61ea.html "SAP BTP provides REST APIs that enable you to perform administrative tasks on the global account, directory, and subaccount level, such as creating or updating subaccounts, monitoring usage information, managing access, and managing service resources.") :arrow_upper_right:

**Related Information**  


[Account Model](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loio8ed4a705efa0431b910056c0acdbf377 "Learn more about the different types of accounts on SAP BTP and how they relate to each other.") :arrow_upper_right:

[Managing Global Accounts Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/667f34ba9222450491c2b848cd17e189.html "Your SAP BTP global account is the entry point for managing the resources, landscape, and entitlements for your departments and projects in a self-service manner.") :arrow_upper_right:

[Managing Directories Using the Cockpit [Feature Set B]](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/f495ac1a62684affbff9f2629fe58bb0.html "Learn how to organize and manage your subaccounts according to your technical and business needs by using directories in the SAP BTP cockpit.") :arrow_upper_right:

[Managing Subaccounts Using the Cockpit](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/55d0b6d8b96846b8ae93b85194df0944.html "Learn how to structure a global account according to your organization’s and project’s requirements with regard to members, authorizations, and entitlements by managing subaccounts.") :arrow_upper_right:

[Cloud Management Tools — Feature Set Overview](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/caf4e4e23aef4666ad8f125af393dfb2.html "Cloud management tools represent the group of technologies designed for managing SAP BTP.") :arrow_upper_right:

[Account Models with Subaccounts](account-models-with-subaccounts-049d331.md "Account Models 1 - 5 show ways to structure your global account into subaccounts. Note that all of them are just examples. They are not mutually exclusive and you can adapt them to your own needs.")

[Account Models With Directories and Subaccounts \[Feature Set B\]](account-models-with-directories-and-subaccounts-feature-set-b-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd "With cloud management tools feature set B, we're introducing a more flexible account structure with directories.")

