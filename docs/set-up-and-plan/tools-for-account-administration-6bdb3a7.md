<!-- loio6bdb3a7170b84254bfaf0df52a112980 -->

# Tools for Account Administration

Not only can you choose an account model that meets your business and technical requirements, you also have a choice of different experiences for creating and managing directories and subaccounts in your global account.

Choose between the following tools:

-   Browser-based user interface: [Account Administration in the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8061ecc529d74465b2b9566a634943ec.html "Learn about frequent administrative tasks you can perform using the SAP BTP cockpit, such as managing global accounts, directories, subaccounts, entitlements, and members.") :arrow_upper_right:

-   Command-line tool: [Account Administration Using the SAP BTP Command Line Interface (btp CLI)](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7c6df2db6332419ea7a862191525377c.html "Use the SAP BTP command line interface (btp CLI) for all account administration tasks, such as creating or updating subaccounts, authorization management, and working with service brokers and platforms. It is an alternative to the SAP BTP cockpit for users who like to work in a terminal or want to automate operations using scripts.") :arrow_upper_right:. Note that the scope of the btp CLI is the administration of the global account, directories, and subaccount. Once you've created an environment instance, you must switch to the environment-specific command-line tool \(for example, the cf CLI, Kyma CLI, or kubectl\).

-   Public REST APIs: [Account Administration Using APIs](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1c8db1483d914cd99047aac5280f61ea.html "SAP BTP provides REST APIs that enable you to perform administrative tasks on the global account, directory, and subaccount level, such as creating or updating subaccounts, monitoring usage information, managing access, and managing service resources.") :arrow_upper_right:

-   Infrastructure-as-Code: There's a [Terraform provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest) available in the Hashicorps registry that you can use to automate your account setup. To learn more, see [Account Administration Using Infrastructure as Code](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8d201e43cd8a46d19aca9071c2faa56d.html "Infrastructure as Code (IaC) automates infrastructure provisioning and management using code. It helps ensure consistency, scalability, versioning, collaboration, and documentation. The Terraform Provider for SAP BTP allows you to provision and manage SAP BTP resources as code, with open-source support.") :arrow_upper_right:.

-   Automation of technical operations tasks: [SAP Automation Pilot](https://help.sap.com/docs/automation-pilot?version=Cloud) is a low code/no code automation engine to reduce operation efforts for apps on SAP BTP and also brings catalogs for automated account setup and management.


**Related Information**  


[Account Administration](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5d62ec89de39442f8f31d527855cbced.html "Learn how to manage global accounts, directories, and subaccounts on SAP BTP using different tools.") :arrow_upper_right:

<a name="loio6dd97e11cae44afa809351e1222aafd8"/>

<!-- loio6dd97e11cae44afa809351e1222aafd8 -->

## Automated SAP BTP Infrastructure Setup

Terraform is the de-facto industry standard for infrastructure as code with more than 3000 providers. With the Terraform provider for SAP BTP, you can now use this standard to create Terraform scripts that set up your SAP BTP landscapes. Given the nature of Terraform, it is even possible to add non-SAP infrastructure to those scripts if the infrastructure provider offers a Terraform provider as well.

The Terraform provider for SAP BTP enables you to automate the provisioning, management, and configuration of resources on SAP BTP. By leveraging this provider, you can simplify and streamline the deployment and maintenance of SAP BTP services and applications. See [Terraform Provider for SAP BTP](https://registry.terraform.io/providers/SAP/btp/latest/docs).

Currently, the Terraform provider for SAP BTP is available for non-productive use and SAP is working with several customers on shaping the first release for productive use. You can check out some of the Terraform scripts in a samples repository in the [GitHub repository for the Terraform Provider for SAP BTP](https://github.com/SAP-samples/btp-terraform-samples).

