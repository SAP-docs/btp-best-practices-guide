<!-- loio5302ea447ecf4c3f8999989088a2c27c -->

# Naming Conventions for SAP BTP Accounts

While naming conventions are specific for each organization and use case, consider the following recommendations and examples.



<a name="loio5302ea447ecf4c3f8999989088a2c27c__section_qvw_fhd_r1c"/>

## Recommended Naming Conventions

-   Each Cloud Foundry org, and respectively, each Kyma cluster, belongs to exactly one subaccount. Thus, it's recommended that you derive the org and cluster names from the subaccount name.

-   Because there's no connection between spaces/namespaces in different subaccounts, we recommend giving identical names to the dev, test, and prod versions of projects and spaces/namespaces.

-   To prevent conflicts with special characters, use lower-case letters and hyphens, and avoid spaces or underscores in names. As an exception, subaccount names may use natural language with capitalization and blank spaces.

-   URLs cannot be longer than 63 characters, so use short names for subaccount, subdomain, Cloud Foundry org and spaces, and Kyma cluster and namespaces. For example, use “prod” instead of “production”.

-   There's no need to mention the company in subaccount names, which are always seen in the context of your global account in the SAP BTP cockpit. However, it's recommended to include the company name in the subdomain and Cloud Foundry org name.

-   If you use directories to group your subaccounts, choose descriptive directory names that reflect the desired distinction - for example, by functional area, location, or subsidiary.




<a name="loio5302ea447ecf4c3f8999989088a2c27c__section_nxz_bxz_knb"/>

## Example: Naming per Functional Area in Cloud Foundry

> ### Recommendation:  
> -   Similar name for a subaccount, its subdomain, and its Cloud Foundry org
> 
> -   Identical names for related Cloud Foundry spaces across the landscapes \(dev, test, prod\)


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

mycompany-IT-dev

</td>
<td valign="top">

mycompany-IT-test

</td>
<td valign="top">

mycompany-IT-prod

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

mycompany-IT-dev

</td>
<td valign="top">

mycompany-IT-test

</td>
<td valign="top">

mycompany-IT-prod

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



<a name="loio5302ea447ecf4c3f8999989088a2c27c__section_hk2_mjd_r1c"/>

## Example: Naming per Functional Area in Kyma

> ### Recommendation:  
> -   Similar name for a subaccount, its subdomain, and its Kyma cluster
> 
> -   Identical names for related Kyma namespaces across the landscapes \(dev+test and prod\)


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
<td valign="top" colspan="6">

dev-test

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

