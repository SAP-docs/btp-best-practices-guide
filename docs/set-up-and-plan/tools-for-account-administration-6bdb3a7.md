<!-- loio6bdb3a7170b84254bfaf0df52a112980 -->

# Tools for Account Administration

Choosing the appropriate tools for account administration on SAP BTP depends on your specific requirements, existing skillset, the complexity of your environment, and on the cloud maturity of your organization.

> ### Recommendation:  
> -   SAP BTP cockpit provides an accessible and graphical interface suitable for general administrative tasks.
> 
> -   The btp CLI and APIs offer powerful automation and integration capabilities to advanced users.
> 
> -   SAP Automation Pilot provides pre-designed automated actions.
> 
> -   Finally, the Terraform Provider for SAP BTP offers scalability and repeatability for complex configurations and sustainable automation.

Understanding the strengths and limitations of these tools is key to optimizing your SAP BTP account administration and ensuring efficient and sustainable operations:

**Tools for Account Administration**


<table>
<tr>
<th valign="top">

Tool Name and Description

</th>
<th valign="top">

Key Features

</th>
<th valign="top">

Recommended Usage Scenarios

</th>
</tr>
<tr>
<td valign="top">

**SAP BTP Cockpit**

\(see [Account Administration in the Cockpit](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8061ecc529d74465b2b9566a634943ec.html "Learn about frequent administrative tasks you can perform using the SAP BTP cockpit, such as managing global accounts, directories, subaccounts, entitlements, and members.") :arrow_upper_right:\)

</td>
<td valign="top">

-   User-friendly graphical, browser-based interface
-   No automation capabilities



</td>
<td valign="top">

-   To start your journey with SAP BTP and explore the options and features that it provides for your organization.
-   To get a graphical overview of your subaccounts and directories, or to explore new services.
-   To create and manage your SAP BTP resources manually.



</td>
</tr>
<tr>
<td valign="top">

**btp CLI**

\(see [Account Administration Using the SAP BTP Command Line Interface (btp CLI)](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7c6df2db6332419ea7a862191525377c.html "Use the SAP BTP command line interface (btp CLI) for all account administration tasks, such as creating or updating subaccounts, authorization management, and working with service brokers and platforms. It is an alternative to the SAP BTP cockpit for users who like to work in a terminal or want to automate operations using scripts.") :arrow_upper_right:\)

</td>
<td valign="top">

-   Command-line tool for managing SAP BTP accounts
-   Can be used for automation and human-interaction alike
-   Moderate learning curve for new users
-   Scope is SAP BTP account management. To manage Cloud Foundry or Kyma content, you need other CLI tools \(cf CLI, Kyma CLI, kubectl\).



</td>
<td valign="top">

-   To start managing SAP BTP in a more concise and understandable approach. However, as a command-line tool, the btp CLI follows an imperative approach and leaves some heavy lifting on your end.
-   To quickly get insights into your SAP BTP setup by running particular commands to get machine-readable outputs.
-   To trigger one-off actions, for example cleaning up a role collection assignment in a subaccount that was set up manually.



</td>
</tr>
<tr>
<td valign="top">

**Public REST APIs**

\(see [Account Administration Using APIs](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1c8db1483d914cd99047aac5280f61ea.html "SAP BTP provides REST APIs that enable you to perform administrative tasks on the global account, directory, and subaccount level, such as creating or updating subaccounts, monitoring usage information, managing access, and managing service resources.") :arrow_upper_right:\)

</td>
<td valign="top">

-   RESTful APIs for programmatically managing SAP BTP components
-   For use with a language of your choice
-   Requires programming skills
-   Different OAuth requirements for different APIs



</td>
<td valign="top">

-   To build your automation of SAP BTP from scratch without using any external framework or tool. However, you then need to deal with authentication flows, error handling, and polling.



</td>
</tr>
<tr>
<td valign="top">

**Terraform Provider for SAP BTP**

\(see [Account Administration Using Infrastructure as Code](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8d201e43cd8a46d19aca9071c2faa56d.html "Infrastructure as Code (IaC) automates infrastructure provisioning and management using code. It helps ensure consistency, scalability, versioning, collaboration, and documentation. The Terraform Provider for SAP BTP allows you to provision and manage SAP BTP resources as code, with open-source support.") :arrow_upper_right: and [SAP BTP - Administrator's Guide Samples\)](https://github.com/SAP-samples/btp-admin-guide-samples)

</td>
<td valign="top">

-   Tools to define and manage infrastructure through code
-   Declarative language
-   Automated deployment and provisioning
-   Consistency and repeatability
-   Requires familiarity with Infrastructure as Code \(IaC\) tools
-   Significant initial setup and learning curve



</td>
<td valign="top">

-   To automate the provisioning and management of your subaccounts in a scalable way.
-   If your company uses Terraform or OpenTofu to set up and manage other cloud accounts like AWS, Azure, or Google Cloud, then we recommend aligning this also for SAP BTP.



</td>
</tr>
<tr>
<td valign="top">

**SAP Automation Pilot**

\(see [SAP Automation Pilot](https://help.sap.com/docs/automation-pilot?version=Cloud)\)

</td>
<td valign="top">

-   A \(payable\) cloud service to reduce technical operation efforts for apps on SAP BTP and for automated account setup and management
-   Can execute commands towards different SAP BTP runtimes, SAP services, and third-party Ops tools
-   Brings catalogs of automated actions that you can compile to larger commands – either in a low-code/no-code manner or using the integrated GenAI command assistant
-   Integrated with SAP Cloud ALM
-   Using its REST API, it can be plugged to any custom service



</td>
<td valign="top">

-   If you want to automate generic or one-time tasks and use predefined templates and a GenAI-based command assistant, SAP Automation Pilot is a fitting tool.
-   If your DevOps and operations teams want to enhance efficiency for running their apps on SAP BTP and SAP BTP resources \(such as SAP HANA Cloud\), for example in terms of alert remediation, maintenance, health checks, automated root cause analysis, operational mass operations.
-   To centrally manage technical ops automation flows from SAP Cloud ALM.



</td>
</tr>
</table>

**Related Information**  


[Account Administration](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5d62ec89de39442f8f31d527855cbced.html "Learn how to manage global accounts, directories, and subaccounts on SAP BTP using different tools.") :arrow_upper_right:

