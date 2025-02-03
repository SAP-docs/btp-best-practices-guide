<!-- loio2db81f42f5194454beecde6cd4994dda -->

# Setting Up Your Account Model

The hierarchical structure between global accounts, directories, and subaccounts lets you define an account model that accurately fits your business and development needs.



> ### Tip:  
> Before you set up your account model and assign users, read [Onboard to SAP Cloud Identity Services](../onboard-to-sap-cloud-identity-services-9c897ee.md).



<a name="loio2db81f42f5194454beecde6cd4994dda__section_avw_5vk_31c"/>

## Global Accounts

Once you've signed your commercial contract with SAP, you'll receive access information and credentials for your **global account**. This global account is the realization of your commercial contract with SAP and you use it to manage the resources and entitlements for your development projects. You'll also receive a bill for all resources used per global account.

If you want to keep a separation, for example, based on commercial model or to match your organization's legal entities, you can choose to have multiple global accounts. Otherwise, using just one global account reduces the administrative effort and technical limitations, for example, when you want to share services between subaccounts.



<a name="loio2db81f42f5194454beecde6cd4994dda__section_tjr_vvk_31c"/>

## Subaccounts

To develop and deploy applications, to use services, and to subscribe to business applications provided by SAP, you must create **subaccounts**. You can create any number of subaccounts in any region, depending on your contract. For example, if you're located in the U.S., you can create subaccounts in different regions, such as Europe \(Rot\) or Japan \(Tokyo\), to support the customers who are using your applications. Subaccounts are independent from each other, which means that each subaccount allows for dedicated quota and user management. You can configure a dedicated identity provider for business users in each subaccount.

> ### Note:  
> If you need to move a subaccount from one global account to another, read [3246456](https://me.sap.com/notes/3246456).



<a name="loio2db81f42f5194454beecde6cd4994dda__section_hjh_wvk_31c"/>

## Directories

If you have many subaccounts, you can use **directories** to keep the overview and simplify administration. Directories group subaccounts and/or further child directories. You can use directories to manage entitlements or users for entire groups of subaccounts. You can distribute the resources that are assigned to the global account via directories to their child subaccounts.



<a name="loio2db81f42f5194454beecde6cd4994dda__section_ety_wvk_31c"/>

## Spaces and Namespaces

Depending on the runtime you plan to use, you may have further possibilities to create a structure within a subaccount; such as **spaces** in Cloud Foundry, or **namespaces** in Kyma. For example, in SAP BTP, Kyma runtime, each subaccount corresponds to provisioning one cluster. You can keep the number of required subaccounts minimal by using namespaces within a cluster to set up the structure according to the requirements of your organization and projects with regards to users and authorizations.

To help you decide for a runtime, see [Develop and Build](../develop-and-build-8a44d9c.md) and [Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/viewer/8cc4e6b957be41d0b7a07680d1d9bb07/Cloud/en-US/de5c964bd17443409e11c55f4f5dacb7.html "In SAP BTP, you have the choice between several runtimes.") :arrow_upper_right:.

> ### Note:  
> The account models suggested in this guide only take into account the platform concepts of global accounts, directories, and subaccounts.
> 
> For runtime-specific information, read:
> 
> -   [Staged Development with the Cloud Foundry Environment](staged-development-with-the-cloud-foundry-environment-1c5f810.md)
> 
> -   [Staged Development with the Kyma Environment](staged-development-with-the-kyma-environment-ec8a269.md)

**Related Information**  


[Account Model with Subaccounts](account-model-with-subaccounts-049d331.md "This simple account model shows how to structure your global account into three subaccounts, without making use of directories. It can later easily be expanded to make use of directories as further structuring elements.")

[Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd "The account models in this section show use cases for directories as structuring elements for your subaccounts.")

[Account Model](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loio8ed4a705efa0431b910056c0acdbf377 "Learn more about the different types of accounts on SAP BTP and how they relate to each other.") :arrow_upper_right:

