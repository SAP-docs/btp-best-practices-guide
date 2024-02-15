<!-- loio1c5f810ac8b84068a6936d02bc9aeea9 -->

# Considerations for the Cloud Foundry Environment

While creating a staged development environment is a good idea in any case, there are some considerations specific to Cloud Foundry you might want to take into account.

> ### Recommendation:  
> In Cloud Foundry, we recommend that you create three subaccounts to set up a staged development environment: one subaccount each for development, testing, and production. To do so, you create subaccounts and enable Cloud Foundry, which essentially creates a Cloud Foundry org.

When you enable the Cloud Foundry environment in one of your subaccounts, the system automatically creates a Cloud Foundry org for you. The subaccount and the org have a 1:1 relationship and the same navigation level in the cockpit \(even though they may have different names\). You can create spaces within that Cloud Foundry org. Spaces let you further break down your account model and use services and functions in the Cloud Foundry environment.

You can use both subaccounts and spaces to develop applications and to use services. You must therefore decide, for example, whether to create different subaccounts or spaces within one subaccount to set up a staged development environment. Consider the following:

-   Think of a subaccount as a tenant: Data access and data visibility segregation is done on subaccount level, not on application or Cloud Foundry space level. Keep in mind that services that are consumed by every app within a subaccount will gather messages from all of these services. If those shouldn't be visible across applications, you need to create different subaccounts.

-   In general, we recommend that you create different subaccounts for a staged development environment. This allows for dedicated user management between the different stages, as well as for dedicated data management in elastic services, such as SAP IoT Application Enablement.

-   You can then create a dedicated space for each application, extension, solution, or other project within these subaccounts if you don't need a dedicated user management for these applications and projects.

-   You can monitor the consumption of resources in your global account only per subaccount, directory, or Cloud Foundry space. Not per application. To monitor the resources consumed by a specific project, department, or application, create a dedicated subaccount, directory, or space for them.

-   Accurate billing is only possible for global accounts. For the consumption-based model, you can calculate costs according to usage, but note that this is only approximate. See [Monitoring Usage and Consumption Costs in Your Global Account](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/de6f0db8919f4e6f97e54bc4ddaf2ab8.html "In a global account that uses the consumption-based commercial model, you can monitor the usage of billed services and your consumption costs in the SAP BTP cockpit.") :arrow_upper_right:.


![](images/sap_cp_lm_account_model_scenarios_1_cf_17b88f0.png)

To decide whether to create separate subaccounts or separate spaces within the same subaccount, consider the different configuration possibilities, available for subaccounts and spaces:


<table>
<tr>
<th valign="top">

Configuration

</th>
<th valign="top">

Subaccount

</th>
<th valign="top">

Space

</th>
</tr>
<tr>
<td valign="top">

Configure your own group of business users

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Configure a Cloud Connector tunnel

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Configure roles and trust

</td>
<td valign="top">

Yes

</td>
<td valign="top">

No

</td>
</tr>
<tr>
<td valign="top">

Assign quotas

</td>
<td valign="top">

Yes \(mandatory\)

</td>
<td valign="top">

Yes

</td>
</tr>
</table>

**Related Information**  


[Create Spaces](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/2f6ed22ccf424dae84345f4500c2d8ea.html "Create spaces in your Cloud Foundry organization using the SAP BTP cockpit.") :arrow_upper_right:

