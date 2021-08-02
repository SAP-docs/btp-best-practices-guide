<!-- loio951d36ce07324f919f74f52b0f9f9e0a -->

# Security Concepts

The level of security you implement may vary depending on your use case and your company's general security requirements. However, there are a few best practices that we recommend, regardless of your implementation.



<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_jp5_q4n_cgb"/>

## General SAP BTP and Network Security Aspects

The SAP BTP landscape runs in an isolated network that is protected from the outside by firewalls, a DMZ, and communication proxies for all inbound and outbound communication. All user access is protected with transport layer security \(TLS\). Use SAP BTP Connectivity to enable your SAP BTP applications to access remote services on the Internet or in your on-premise systems. For connecting to Internet services, we recommend that you use APIs with destinations, and for cloud-to-on-premise scenarios, we recommend that you use destinations and the Cloud Connector. If you use destinations, you achieve a separation between the application and the configuration, which means it's easier to make configuration changes. And you can use the destinations to store credentials and certificates.

The Cloud Connector is a lightweight on-premise agent that establishes a tunnel for connecting your cloud applications to on-premise systems. The Cloud Connector acts as a reverse invoke between the on-premise network and SAP BTP. That means you don't need to open in-bound ports in the firewall for external access from the cloud. The Cloud Connector provides a fine-granular access control mechanism, supports multiple protocols, such as RFC and HTTP, and can forward the cloud user identity using principal propagation. It enables users to log on to on-premise systems without logging in again by forwarding their logged-on identity from the cloud. You can configure the Cloud Connector directly from the subaccount in the SAP BTP cockpit.

For more information, see:

-   [f70fcf1c2d0a4a979adfe44cebc93c20.md](f70fcf1c2d0a4a979adfe44cebc93c20.md)

-    [Connectivity](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e54cc8fbbb571014beb5caaf6aa31280.html) 

-   [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html)




<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_jm5_1nw_jgb"/>

## Identity Management and Authorization Management

Restrict access to any endpoint of your application through authentication and authorization. This ensures that only the intended target group, such as your company's employees, can access your application. We recommend that you use SAP BTP's default SAML or OpenID Connect single sign-on protocol for user acccess and principal propagation for back-end access. If only access for technical users is needed, however, principal propagation is not necessary. Once a user is authenticated, single sign-on propagates the credentials to the back-end system without requiring the user to reauthenticate.

Subaccounts get their users from identity providers. Administrators ensure that users can access only their subaccounts by establishing a dedicated trust relationship between the identity providers and the respective subaccounts. The preconfigured default identity provider for SAP BTP is SAP ID Service. SAP ID Service is managed by SAP. You can also connect your own identity provider, which means you have full control over your user base. For developing and administrating your own applications on SAP BTP, we recommend that you use [SAP BTP Identity Authentication](https://help.sap.com/viewer/p/IDENTITY_AUTHENTICATION) in your own tenant. Identity Authentication is SAP's cloud solution for identity lifecycle management for SAP BTP applications, and optionally for on-premise applications.

> ### Recommendation:  
> We recommend that you use SAP Cloud Identity Services - Identity Authentication as a hub, especially if your business users are stored in multiple corporate identity providers.
> 
> For this scenario, connect Identity Authentication as single custom identity provider to SAP BTP. Next use Identity Authentication to integrate your corporate identity providers.
> 
> For more information, see [Corporate Identity Providers](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/19f3eca47db643b6aad448b5dc1075ad.html) and [Configure Conditional Authentication for an Application](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/0143dce88a604533ab5ab17e639fec09.html) in [What Is Identity Authentication](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/27882717f44b445fa287936c6f43dc1f.html) and [SAP Cloud Identity Services - Identity Authentication](https://help.sap.com/viewer/product/IDENTITY_AUTHENTICATION/Cloud/en-US)

See the following for more information about security best practices:

-   [Setting Up Authentication](Setting_Up_Authentication_1dbce9c.md)
-   [Setting Up Authorization](Setting_Up_Authorization_cb9f0ac.md)
-   [Setting Up Identity Propagation](Setting_Up_Identity_Propagation_12cf719.md)



<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_ex2_25n_cgb"/>

## Security Considerations for Applications

When building applications, your developers should use the security features of SAP BTP, such as protection from web attacks. We recommend that your developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the cockpit. SAP BTP offers platform roles that help you ensure a segregation of duties, such as between app development and administration.

It's likely that data protection and privacy influence your architecture and the functions of your application, and you should consider any implications as early as possible in your development process. Security monitoring is done with audit logging. SAP BTP writes logs for security-relevant events and the written log files are digitally signed to ensure their integrity.

See the following for more information about security best practices:

-   [52750a8f86bb428ca224daa4312d122e.md](52750a8f86bb428ca224daa4312d122e.md)

-   [Giving Access Rights to Platform Users](Giving_Access_Rights_to_Platform_Users_a03d08e.md)
-   [7e513d31704a4a87831191e504ca850a.md](7e513d31704a4a87831191e504ca850a.md)


