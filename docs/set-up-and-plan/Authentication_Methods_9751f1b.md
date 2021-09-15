<!-- loio9751f1b234ac4024a173887c67df1f0d -->

# Authentication Methods

You can implement the authentication methods that are available on SAP BTP on the frontend of applications.

<a name="loio9751f1b234ac4024a173887c67df1f0d__table_qsd_fhg_l2b"/>Authentication Methods on SAP BTP


<table>
<tr>
<th>

Authentication Method



</th>
<th>

Default Options



</th>
<th>

Description



</th>
</tr>
<tr>
<td>

FORM or SAML2



</td>
<td>

Trusted SAML 2.0 identity provider with application-to-application SSO



</td>
<td>

FORM authentication implemented through the Security Assertion Markup Language \(SAML\) 2.0 protocol. Authentication is delegated to the SAP ID service or a custom identity provider.



</td>
</tr>
<tr>
<td>

BASIC



</td>
<td>

User name and password



</td>
<td>

HTTP basic authentication delegated to the SAP ID service or to an on-premise SAP NetWeaver AS Java system. Web browsers prompt users to enter a user name and password. By default, the SAP ID service is used.



</td>
</tr>
<tr>
<td>

CERT



</td>
<td>

Client certificate



</td>
<td>

Used for authentication only with client certificate.



</td>
</tr>
<tr>
<td>

BASICCERT



</td>
<td>

User name and password client certificate



</td>
<td>

Used for authentication either with a client certificate or with user name and password.



</td>
</tr>
<tr>
<td>

OAUTH



</td>
<td>

OAuth 2.0 token



</td>
<td>

Authentication according to the OAuth 2.0 protocol with an OAuth access token.



</td>
</tr>
<tr>
<td>

OpenID-Connect \(OIDC\)



</td>
<td>

OIDC token



</td>
<td>

A simple identity layer on top of the OAuth 2.0 protocol that allows clients to verify the identity of the end user based on the authentication performed by an identity provider, as well as to obtain basic profile information about the user.



</td>
</tr>
</table>

Authentication methods depend on buildpacks, and the Cloud Foundry environment offers more than just Java. Please refer to the [SAP Authorization and Trust Management Service in the Cloud Foundry environment](https://help.sap.com/viewer/50fd4b19521f4bec9ee9cc6c72a90872//en-US/6373bb7a96114d619bfdfdc6f505d1b9.html "The global account and subaccounts get their users from identity providers. Administrators make sure that users can only access their dedicated subaccount by making sure that there is a dedicated trust relationship only between the identity providers and the respective subaccounts. Developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the SAP BTP cockpit.") :arrow_upper_right: documentation for more information.

