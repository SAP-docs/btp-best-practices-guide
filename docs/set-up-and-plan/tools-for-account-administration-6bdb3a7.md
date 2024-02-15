<!-- loio6bdb3a7170b84254bfaf0df52a112980 -->

# Tools for Account Administration

Not only can you choose an account model that meets your business and technical requirements, you also have a choice of different experiences for creating directories and subaccounts in your global account.

Choose between the following tools:

-   Browser-based user interface: [Account Administration in the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8061ecc529d74465b2b9566a634943ec.html "Learn about frequent administrative tasks you can perform using the SAP BTP cockpit, such as managing global accounts, directories, subaccounts, entitlements, and members.") :arrow_upper_right:

-   Command-line tool: [Account Administration Using the SAP BTP Command Line Interface (btp CLI)](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7c6df2db6332419ea7a862191525377c.html "Use the SAP BTP command line interface (btp CLI) for all account administration tasks, such as creating or updating subaccounts, authorization management, and working with service brokers and platforms. It is an alternative to the SAP BTP cockpit for users who like to work in a terminal or want to automate operations using scripts.") :arrow_upper_right:. Note that the scope of the btp CLI is the administration of the global account, directories, and subaccount. Once you've created an environment instance, you must switch to the environment-specific command-line tool \(for example, the cf CLI, Kyma CLI, or kubectl\).

-   Public REST APIs: [Account Administration Using APIs](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1c8db1483d914cd99047aac5280f61ea.html "SAP BTP provides REST APIs that enable you to perform administrative tasks on the global account, directory, and subaccount level, such as creating or updating subaccounts, monitoring usage information, managing access, and managing service resources.") :arrow_upper_right:

-   There is a [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest) available in the Hashicorps registry that you can use to automate your account setup. Note that it is still in beta. If you're not familiar with Terraform, you can check out the samples and best practices in this [GitHub repository](https://github.com/SAP-samples/btp-terraform-samples).


For information about creating subaccounts in the SAP BTP cockpit, see [Create a Subaccount](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/05280a123d3044ae97457a25b3013918.html "Create subaccounts in your global account using the SAP BTP cockpit.") :arrow_upper_right:. For the same procedure using the btp CLI, see [Create a Subaccount Using the btp CLI](https://help.sap.com/docs/btp/btp-cli-command-reference/btp-create-accounts-subaccount).

**Related Information**  


[Managing Global Accounts Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/667f34ba9222450491c2b848cd17e189.html "Your SAP BTP global account is the entry point for managing the resources, landscape, and entitlements for your departments and projects in a self-service manner.") :arrow_upper_right:

[Managing Directories Using the Cockpit \[Feature Set B\]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f495ac1a62684affbff9f2629fe58bb0.html "Learn how to organize and manage your subaccounts according to your technical and business needs by using directories in the SAP BTP cockpit.") :arrow_upper_right:

[Managing Subaccounts Using the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/55d0b6d8b96846b8ae93b85194df0944.html "Learn how to structure a global account according to your organization’s and project’s requirements with regard to members, authorizations, and entitlements by managing subaccounts.") :arrow_upper_right:

