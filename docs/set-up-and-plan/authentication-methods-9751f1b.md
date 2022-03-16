<!-- loio9751f1b234ac4024a173887c67df1f0d -->

# Authentication Methods

You can implement the authentication methods that are available on SAP BTP on the frontend of applications.

<a name="loio9751f1b234ac4024a173887c67df1f0d__table_qsd_fhg_l2b"/>Authentication Methods on SAP BTP


<table>
<tr>
<th valign="top">

Authentication Method



</th>
<th valign="top">

Default Options



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

FORM or SAML2



</td>
<td valign="top">

Trusted SAML 2.0 identity provider with application-to-application SSO



</td>
<td valign="top">

FORM authentication implemented through the Security Assertion Markup Language \(SAML\) 2.0 protocol. Authentication is delegated to the SAP ID service or a custom identity provider.



</td>
</tr>
<tr>
<td valign="top">

BASIC



</td>
<td valign="top">

User name and password



</td>
<td valign="top">

HTTP basic authentication delegated to the SAP ID service or to an on-premise SAP NetWeaver AS Java system. Web browsers prompt users to enter a user name and password. By default, the SAP ID service is used.



</td>
</tr>
<tr>
<td valign="top">

CERT



</td>
<td valign="top">

Client certificate



</td>
<td valign="top">

Used for authentication only with client certificate.



</td>
</tr>
<tr>
<td valign="top">

BASICCERT



</td>
<td valign="top">

User name and password client certificate



</td>
<td valign="top">

Used for authentication either with a client certificate or with user name and password.



</td>
</tr>
<tr>
<td valign="top">

OAUTH



</td>
<td valign="top">

OAuth 2.0 token



</td>
<td valign="top">

Authentication according to the OAuth 2.0 protocol with an OAuth access token.



</td>
</tr>
<tr>
<td valign="top">

OpenID-Connect \(OIDC\)



</td>
<td valign="top">

OIDC token



</td>
<td valign="top">

A simple identity layer on top of the OAuth 2.0 protocol that allows clients to verify the identity of the end user based on the authentication performed by an identity provider, as well as to obtain basic profile information about the user.



</td>
</tr>
</table>

Authentication methods depend on buildpacks, and the Cloud Foundry environment offers more than just Java. Please refer to the [SAP Authorization and Trust Management Service in the Cloud Foundry environment](https://help.sap.com/viewer/ae8e8427ecdf407790d96dad93b5f723/Cloud/en-US/6373bb7a96114d619bfdfdc6f505d1b9.html "The global account and subaccounts get their users from identity providers. Administrators make sure that users can only access their dedicated subaccount by making sure that there is a dedicated trust relationship only between the identity providers and the respective subaccounts. Developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the SAP BTP cockpit.") :arrow_upper_right: documentation for more information.

