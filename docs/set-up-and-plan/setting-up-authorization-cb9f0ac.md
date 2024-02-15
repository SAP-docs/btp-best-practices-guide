<!-- loiocb9f0ac174a248c4bc7391e5bf5a0b1a -->

# Setting Up Authorization

The methods for assigning authorizations on SAP BTP include manual assignment, federation, and provisioning. In practice, you use all these methods according to the situation.

When your system has many users in widely used production accounts, identity federation or provisioning is the preferred method. We recommend provisioning over federation where possible.

**Methods for Assigning Authorizations**


<table>
<tr>
<th valign="top">

Method

</th>
<th valign="top">

Provisioning

</th>
<th valign="top">

Federation

</th>
</tr>
<tr>
<td valign="top">

Description

</td>
<td valign="top">

Provisioning synchronizes users between source systems and target systems based on rules or processes. Individual authorizations are assigned to business roles. When a user needs access a target system, the automation makes sure to assign all the required authorizations defined by the business role in the target system. For example, when a new hire is assigned to a sales organization in an HR system, provisioning triggers the creation of the user in the target sales system with the required authorizations.

Provision user data with tools like Identity Provisioning and the SAP Cloud Identity Access Governance service.

</td>
<td valign="top">

Federation is an agreement between the administrator of the identity provider and the administrator of the system that consume it. The agreement specifies what attributes to include in tokens used to authenticate users in the relying system. The administrator of the relying system assigns authorizations indirectly on the attributes the identity provider sends. For example, an identity provider includes the user groups attribute in authentication tokens it issues. The administrator of the relying system maps authorizations for sales applications to any user who belongs to the *sales* user group and not to individual users.

Use tools such as the command-line interface \(btp CLI\) or the SAP BTP cockpit

</td>
</tr>
<tr>
<td valign="top">

Restrictions

</td>
<td valign="top">

Provisioning is partially available for platform users. In Feature Set B, role collections on the subaccount level can be provisioned, such as *Subaccount Administrator*.

</td>
<td valign="top">

The ABAP environment doesn't support federation.

</td>
</tr>
<tr>
<td valign="top">

Advantages

</td>
<td valign="top">

Centrally defined business roles define which authorizations belong together.

Approval workflows for authorizations.

When a user changes their job or leaves the organization, provisioning can remove the user data from target systems in accordance with compliance rules.

</td>
<td valign="top">

Simpler to implement than provisioning.

Authorization information comes with the authentication token. The user has information about their authorizations as soon as the changes have been made in the identity provider.

</td>
</tr>
<tr>
<td valign="top">

Disadvantages

</td>
<td valign="top">

To get authorizations in a system, the user must wait until a provisioning job has run to update the target system.

</td>
<td valign="top">

Doesn't scale like provisioning.

Information that authorizations belong together can only be achieved manually.

When a user is removed from the identity provider, the user can't log on, but their user data remains in the relying systems. You must actively ensure the deletion of the remaining data.

</td>
</tr>
</table>

> ### Remember:  
> There are two types of users on SAP BTP: platform and business. Platform users are usually developers, administrators, or operators who deploy, administer, and troubleshoot applications and services. Business users are those users who consume the applications that are deployed to SAP BTP.
> 
> In addition to subaccount authorizations \(role collections\), assign roles for the environment.
> 
> For more information, see [Giving Access Rights to Platform Users](giving-access-rights-to-platform-users-a03d08e.md).

**Related Information**  


[Mapping Role Collections in the Subaccount](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/9e1bf57130ef466e8017eab298b40e5e.html)

[Role Collections and Roles in Global Accounts, Directories, and Subaccounts \[Feature Set B\]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/0039cf082d3d43eba9200fe15647922a.html "In the cloud management tools feature set B, SAP BTP provides a set of role collections to set up administrator access to your global account and subaccounts.") :arrow_upper_right:

[Setting Up Identity Lifecycle](setting-up-identity-lifecycle-2c30208.md "As people join, change roles, and eventually leave your organization, you care for the onboarding, maintenance, and offboarding of their users in your systems. If you're a small organization, you can use manual processes, otherwise you need to automate.")

[Onboard to SAP Cloud Identity Services](../onboard-to-sap-cloud-identity-services-9c897ee.md "When setting up accounts, you need to assign users. While we provide you with your first users to get you started, your organization has identity providers that you want to integrate.")

