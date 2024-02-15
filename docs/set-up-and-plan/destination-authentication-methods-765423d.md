<!-- loio765423ddb66147bc8141607a8522fe65 -->

# Destination Authentication Methods

Destinations are part of SAP BTP Connectivity and are used for communication between a cloud application and a remote system.

Destinations are required to consume a target remote service from an application. They're resolved at runtime based on their symbolic names, resulting in an object that contains customer-specific configuration details, such as the URL of the remote system or service, the authentication type, and the respective credentials.

**Destination Authentication Methods on SAP BTP**


<table>
<tr>
<th valign="top">

Authentication Method

</th>
<th valign="top">

Description

</th>
<th valign="top">

Environment

</th>
<th valign="top">

Internet Proxy

</th>
<th valign="top">

On-Premise Proxy

</th>
</tr>
<tr>
<td valign="top">

AppToAppSSO

</td>
<td valign="top">

Used for application-to-application communication if the caller needs to propagate its logged-in user. Both applications must be deployed on SAP BTP.

</td>
<td valign="top">

Neo

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

BasicAuthentication

</td>
<td valign="top">

Used for destinations that refer to a service on the Internet or an on-premise system that requires basic authentication.

</td>
<td valign="top">

Neo and Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

ClientCertificateAuthentication

</td>
<td valign="top">

Uses a technical user certificate to perform mutual transport layer security \(TLS\) authentication.

</td>
<td valign="top">

Neo and Cloud Foundry

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

NoAuthentication

</td>
<td valign="top">

Used for destinations that refer to a service on the Internet or an on-premise system that doesn't require authentication.

</td>
<td valign="top">

Neo and Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

OAuth2SAMLBearerAssertion

</td>
<td valign="top">

Enables applications to use SAML assertions to access OAuth-protected resources.

</td>
<td valign="top">

Neo and Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

PrincipalPropagation

</td>
<td valign="top">

Forwards the identity of an on-demand user to the Cloud Connector, and from there to the back end of the relevant on-premise system.

</td>
<td valign="top">

Neo and Cloud Foundry

</td>
<td valign="top">

No

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

OAuth2ClientCredentials

</td>
<td valign="top">

Used to request an access token from an OAuth authorization server, using the `client_credentials` grant.

The retrieved access token is cached and auto-renovated. When a token is about to expire, a new token is created shortly before the expiration of the old one.

</td>
<td valign="top">

Neo and Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

OAuth2UserTokenExchange

</td>
<td valign="top">

Using this authentication type, the destination service performs all the user token exchange steps automatically, which lets you simplify your application development.

This enables you to use a user token that you already have, in order to fetch a token from a different OAuth client, in the context of the same tenant.

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

OAuth2Password

</td>
<td valign="top">

Provides support for applications to use the OAuth password grant flow for consuming OAuth-protected resources.

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

OAuth2JWTBearer

</td>
<td valign="top">

To allow an application to call another application, pass the user context, and fetch resources, the caller application must pass an access token. In this authorization flow, the initial user token is passed to the OAuth server as input data. This process is performed automatically by the destination service, which helps to simplify application development.

This enables you to use a user token that you already have, in order to fetch a token from a different OAuth client, in the context of the same tenant.

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
<tr>
<td valign="top">

SAMLAssertion

</td>
<td valign="top">

Retrieves a generated SAML assertion from the destination service.

</td>
<td valign="top">

Cloud Foundry

</td>
<td valign="top">

Yes

</td>
<td valign="top">

Yes

</td>
</tr>
</table>

> ### Recommendation:  
> For user token exchange, use the OAuth2JWTBearer authentication method when possible, as OAuth2UserTokenExchange needs a two-step mechanism to achieve the same resolution.
> 
> Avoid using BasicAuthentication and OAuth2Password in production environments. However, they work well for test environments.

See the following for more information:

-   [HTTP Destinations (Cloud Foundry Environment)](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/42a0e6b966924f2e902090bdf435e1b2.html "Find information about HTTP destinations for Internet and on-premise connections (Cloud Foundry environment).") :arrow_upper_right:

-   [HTTP Destinations (Neo Environment)](https://help.sap.com/viewer/b865ed651e414196b39f8922db2122c7/Cloud/en-US/b068356dd7c34cf7ad6b6023deeb317d.html "") :arrow_upper_right:

