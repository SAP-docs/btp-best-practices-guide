<!-- loio5302ea447ecf4c3f8999989088a2c27c -->

# Naming and Directory Templates

While naming conventions are specific for each organization and use case, the following recommendations and examples might help you. To establish a process for the creation of new directories, consider using a template.



<a name="loio5302ea447ecf4c3f8999989088a2c27c__section_qvw_fhd_r1c"/>

## Recommended Naming Conventions

-   Each Cloud Foundry org, and respectively, each Kyma cluster, belongs to exactly one subaccount. Thus, it's recommended that you use a consistent naming pattern across subaccount, subdomain, and org or cluster name - example, by lowercasing the subaccount name and replacing spaces with hyphens.

-   Because spaces and namespaces in different subaccounts are independent of each other, you can safely reuse names across your DEV, TEST, and PROD subaccounts. We recommend using a consistent naming pattern across environments to make it easier to identify corresponding resources.

-   To prevent conflicts with special characters, use lower-case letters and hyphens, and avoid spaces or underscores in names. As an exception, subaccount names can contain capitalization and blank spaces.

-   You don't need to include the company name in subaccount names, because subaccounts are always displayed in the context of your global account in the SAP BTP cockpit. However, we recommend including the company name or an abbreviation of it in subdomains and Cloud Foundry org names.

-   If you use directories to group your subaccounts, choose descriptive directory names that reflect the desired distinction - for example, by functional area, location, or subsidiary.

-   Individual segments of a hostname \(DNS labels\) are limited to 63 characters. In SAP BTP, application routes combine multiple naming components into a single label, for example, `{CF_ORG}-{CF_SPACE}-{APPNAME}` in Cloud Foundry. The more components are combined, the shorter each individual name must be. Use short names for subaccounts, subdomains, Cloud Foundry orgs and spaces, Kyma namespaces, and application modules. For example, use “prod” instead of “production”. If you exceed the limit, you can configure a custom route in the deployment descriptor \(for example, `mta.yaml` or `values.yaml`; for details, see [Routes](https://help.sap.com/docs/btp/sap-business-technology-platform/mta-routes?locale=en-US&version=Cloud)\) or use the [Custom Domain Service](https://discovery-center.cloud.sap/serviceCatalog/custom-domain?service_plan=custom-domain&region=all&commercialModel=btpea).


> ### Caution:  
> Don't enter personal data in any of these fields. For details, see [Data Protection and Privacy](https://help.sap.com/docs/btp/sap-business-technology-platform/data-protection-and-privacy?state=DRAFT&locale=en-US#generic-fields).



### Example: Naming per Functional Area in Cloud Foundry

> ### Recommendation:  
> -   Similar name for a subaccount, its subdomain, and its Cloud Foundry org
> 
> -   Identical names for related Cloud Foundry spaces across the landscapes \(DEV, TEST, PROD\)


<table>
<tr>
<td valign="top">

Directory

</td>
<td valign="top" colspan="3">

HR

</td>
<td valign="top" colspan="3">

Sales

</td>
<td valign="top" colspan="3">

IT

</td>
</tr>
<tr>
<td valign="top">

Subaccounts

</td>
<td valign="top">

HR Dev

</td>
<td valign="top">

HR Test

</td>
<td valign="top">

HR Prod

</td>
<td valign="top">

Sales Dev

</td>
<td valign="top">

Sales Test

</td>
<td valign="top">

Sales Prod

</td>
<td valign="top">

IT Dev

</td>
<td valign="top">

IT Test

</td>
<td valign="top">

IT Prod

</td>
</tr>
<tr>
<td valign="top">

Subdomains

</td>
<td valign="top">

mycompany-hr-dev

</td>
<td valign="top">

mycompany-hr-test

</td>
<td valign="top">

mycompany-hr-prod

</td>
<td valign="top">

mycompany-sales-dev

</td>
<td valign="top">

mycompany-sales-test

</td>
<td valign="top">

mycompany-sales-prod

</td>
<td valign="top">

mycompany-it-dev

</td>
<td valign="top">

mycompany-it-test

</td>
<td valign="top">

mycompany-it-prod

</td>
</tr>
<tr>
<td valign="top">

Cloud Foundry Orgs

</td>
<td valign="top">

mycompany-hr-dev

</td>
<td valign="top">

mycompany-hr-test

</td>
<td valign="top">

mycompany-hr-prod

</td>
<td valign="top">

mycompany-sales-dev

</td>
<td valign="top">

mycompany-sales-test

</td>
<td valign="top">

mycompany-sales-prod

</td>
<td valign="top">

mycompany-it-dev

</td>
<td valign="top">

mycompany-it-test

</td>
<td valign="top">

mycompany-it-prod

</td>
</tr>
<tr>
<td valign="top">

Spaces

</td>
<td valign="top">

project-portal

activity-recording

</td>
<td valign="top">

project-portal

activity-recording

</td>
<td valign="top">

project-portal

activity-recording

</td>
<td valign="top">

customer-acquisition

sales-support

</td>
<td valign="top">

customer-acquisition

sales-support

</td>
<td valign="top">

customer-acquisition

sales-support

</td>
<td valign="top">

it-support

central-service

</td>
<td valign="top">

it-support

central-service

</td>
<td valign="top">

it-support

central-service

</td>
</tr>
</table>



### Example: Naming per Functional Area in Kyma

> ### Recommendation:  
> -   Similar name for a subaccount, its subdomain, and its Kyma clusters
> 
> -   Use a consistent base name for related Kyma namespaces across landscapes \(for example, “hr”\). Within a shared cluster, add a stage suffix \(“hr-dev”, “hr-test”\) to distinguish environments that coexist in the same cluster. In a dedicated production cluster, the suffix is unnecessary \(“hr”\).


<table>
<tr>
<td valign="top">

Subaccounts

</td>
<td valign="top" colspan="6">

Dev Test

</td>
<td valign="top" colspan="3">

Prod

</td>
</tr>
<tr>
<td valign="top">

Subdomains

</td>
<td valign="top" colspan="6">

mycompany-dev-test

</td>
<td valign="top" colspan="3">

mycompany-prod

</td>
</tr>
<tr>
<td valign="top">

Kyma Clusters

</td>
<td valign="top" colspan="4">

dev-test-1

</td>
<td valign="top" colspan="2">

dev-test-2

</td>
<td valign="top" colspan="3">

prod

</td>
</tr>
<tr>
<td valign="top">

Namespaces

</td>
<td valign="top">

hr-dev

</td>
<td valign="top">

hr-test

</td>
<td valign="top">

sales-dev

</td>
<td valign="top">

sales-test

</td>
<td valign="top">

it-dev

</td>
<td valign="top">

it-test

</td>
<td valign="top">

hr

</td>
<td valign="top">

sales

</td>
<td valign="top">

it

</td>
</tr>
</table>



<a name="loio5302ea447ecf4c3f8999989088a2c27c__section_alg_xzh_q2c"/>

## Template for New Directories

We recommend that you create a process for the creation of new directories. You can use the following example template or adapt it to meet your requirements:


<table>
<tr>
<th valign="top" colspan="2">

New Directory

</th>
</tr>
<tr>
<td valign="top">

Name

</td>
<td valign="top">

Follow your company's naming guidelines - for example, a name reflecting the functional area, location, or subsidiary.

</td>
</tr>
<tr>
<td valign="top">

Owners

</td>
<td valign="top">

We recommend appointing at least two owners.

</td>
</tr>
<tr>
<td valign="top">

Description

</td>
<td valign="top">

Document the following:

-   Target developer audience \(LoB or department\)

-   Types of applications to be developed

-   Runtimes to be used

-   Subscriptions to be used




</td>
</tr>
<tr>
<td valign="top">

Cost center

</td>
<td valign="top">

Define accounting requirements.

</td>
</tr>
<tr>
<td valign="top">

Enrollment

</td>
<td valign="top">

Describe how development projects can enroll in your directory. For details, see [Creating an Onboarding Process for Development Projects](creating-an-onboarding-process-for-development-projects-4bd29a8.md).

</td>
</tr>
</table>

