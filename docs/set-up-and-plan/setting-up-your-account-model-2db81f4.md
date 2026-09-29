<!-- loio2db81f42f5194454beecde6cd4994dda -->

# Setting Up Your Account Model

Your account model defines how you organize global accounts, directories, and subaccounts in SAP BTP to match your business and development needs.

Set up your account model to match your company's structure and development process. Start with the basic three-stage model \(development, testing, production\) and extend as needed. SAP BTP provides tools to manage your landscape at any scale.

Before you set up your account model, you need a global account and the appropriate administrative permissions. For details, see [Account Model](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loio8ed4a705efa0431b910056c0acdbf377 "Learn more about the different types of accounts on SAP BTP and how they relate to each other.") :arrow_upper_right:.

The hierarchical structure between global accounts, directories, and subaccounts lets you define an account model that accurately fits your business and development needs.

> ### Remember:  
> -   A **global account** is the realization of a contract you or your company has made with SAP.
> -   With **directories**, you can organize and manage your subaccounts according to your technical and business needs. 
> -   In **subaccounts**, you deploy applications, use services, and manage your subscriptions. You can use them to manage members, authorizations, and entitlements.
> 
> For details about the SAP BTP account levels, see [Account Model](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loio8ed4a705efa0431b910056c0acdbf377 "Learn more about the different types of accounts on SAP BTP and how they relate to each other.") :arrow_upper_right:.

The following sections walk you through three levels of complexity: a basic three-stage model, a multi-team setup with directories, and a fully customized structure. To draft your specific account model, see [Checklist: Drafting Your Account Model](checklist-drafting-your-account-model-7f1c318.md).



<a name="loio2db81f42f5194454beecde6cd4994dda__section_basic_account_model"/>

## The Basic Account Model

In the cloud \(just like on premise\), we recommend a **staged development process** to qualify changes before bringing them to production. Typically, this means having one global account and creating one subaccount each for development, testing, and production.

![Basic account model: one global account with three subaccounts for DEV, TEST, and PROD](images/Image_Map_Basic_Account_Model_f6bfc5b.png)



### DEV Subaccount

For development purposes and for testing individual increments in the cloud.



### TEST Subaccount

For integration testing in a production-like environment before release. In highly DevOps-driven companies, the TEST subaccount also serves production workloads. In that case, all testing happens in the DEV subaccount.



### PROD Subaccount

For production applications.

> ### Tip:  
> If you're using SAP BTP, Kyma runtime, you might want to combine DEV and TEST in one subaccount. For details, see [Cloud Foundry, Kyma, or Both?](cloud-foundry-kyma-or-both-ec8a269.md)



<a name="loio2db81f42f5194454beecde6cd4994dda__section_typical_account_model"/>

## The Basic Account Model in Action

It's very common to set up your account model not only according to development stages: You might also want to reflect another aspect of your company's organization, for example, functional units like HR, Sales, and IT.

In this case, you can choose to create a set of DEV, TEST, and PROD subaccounts for each functional unit.

Additionally, you can set up one or more subaccounts for services that are shared between teams, such as SAP HANA Cloud, SAP Integration Suite, or SAP Build Work Zone. For details, see [Sharing SAP BTP Services](sharing-sap-btp-services-9fe7e16.md).

At this scale, directories help you group subaccounts and simplify administration. For details, see [Directories](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loioa92721fc75524ec09a7a7255997dbd94 "With directories, you can organize and manage your subaccounts according to your technical and business needs.") :arrow_upper_right:.

![Extended account model: directories grouping DEV, TEST, and PROD subaccount sets per functional unit, plus a shared-services subaccount](images/Account_Model_-_Functional_w_Directories_e8b3e42.png)

The diagram shows three directories \(HR, Sales, IT\), each containing DEV, TEST, and PROD subaccounts, plus a shared-services subaccount outside the directories.

> ### Tip:  
> If you're using SAP BTP, Kyma runtime, you could also consider setting up namespaces for each functional area within the clusters of your DEV, TEST, and PROD subaccounts. The idea is the same, but separation happens on namespace level instead of subaccount level. For details, see [Sharing Kyma Clusters](sharing-kyma-clusters-57ec1ea.md).



<a name="loio2db81f42f5194454beecde6cd4994dda__section_custom_account_model"/>

## Design the Account Model Matching Your Needs

You can add more structuring criteria beyond development stage and functional unit. For example, separate your accounts by location or subsidiary, ideally grouped with directories.

![Custom account model: directories grouping subaccounts by development stage, functional unit, and location or subsidiary](images/Account_Model_-_Layered_Directories_2_99f0925.png)

The diagram adds a location layer: top-level directories for each subsidiary \(for example, US and Germany\), each containing functional-unit directories with their own DEV, TEST, and PROD subaccounts.

> ### Tip:  
> Use **directories** as your primary structuring mechanism. As the term implies, they fulfill the same purpose as a folder hierarchy you'd use to group files. Additionally, you can use directories to manage users and/or entitlements. For details, see [Directories](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loioa92721fc75524ec09a7a7255997dbd94 "With directories, you can organize and manage your subaccounts according to your technical and business needs.") :arrow_upper_right:.
> 
> If you need an additional, flexible grouping and reporting mechanism, assign **labels** to your subaccounts and directories. For details, see [Labels](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loioe8663c08ead648faa673b0d63c5b478e "Labels are user-defined words or phrases that you can assign to various entities in SAP BTP to categorize them in your global account, to identify them more easily.") :arrow_upper_right:.
> 
> Within subaccounts, use **spaces** \(Cloud Foundry\) and **namespaces** \(Kyma\) for further structuring. For details, see [Subaccounts or Spaces/Namespaces?](subaccounts-or-spaces-namespaces-4cb5276.md)

**Related Information**  


[Checklist: Drafting Your Account Model](checklist-drafting-your-account-model-7f1c318.md "Before you start creating subaccounts, take the time to research and draft your desired account model. This guide helps you find out the criteria to tailor the account model to your company's needs.")

