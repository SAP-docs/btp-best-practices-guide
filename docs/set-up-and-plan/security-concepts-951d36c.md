<!-- loio951d36ce07324f919f74f52b0f9f9e0a -->

# Security Concepts

The level of security you implement may vary depending on your use case and your company's general security requirements. However, there are a few best practices that we recommend, regardless of your implementation.



<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_jp5_q4n_cgb"/>

## General SAP BTP and Network Security Aspects

The SAP BTP landscape runs in an isolated network that is protected from the outside by firewalls, a DMZ, and communication proxies for all inbound and outbound communication. All user access is protected with transport layer security \(TLS\). Use SAP BTP Connectivity to enable your SAP BTP applications to access remote services on the Internet or in your on-premise systems. For connecting to Internet services, we recommend that you use APIs with destinations, and for cloud-to-on-premise scenarios, we recommend that you use destinations and the Cloud Connector. If you use destinations, you achieve a separation between the application and the configuration, which means it's easier to make configuration changes. And you can use the destinations to store credentials and certificates.

The Cloud Connector is a lightweight on-premise agent that establishes a tunnel for connecting your cloud applications to on-premise systems. The Cloud Connector acts as a reverse invoke between the on-premise network and SAP BTP. That means you don't need to open in-bound ports in the firewall for external access from the cloud. The Cloud Connector provides a fine-granular access control mechanism, supports multiple protocols, such as RFC and HTTP, and can forward the cloud user identity using principal propagation. It enables users to log on to on-premise systems without logging in again by forwarding their current identity from the cloud. You can configure the Cloud Connector directly from the subaccount in the SAP BTP cockpit.

For more information, see:

-   [Principal Propagation](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/f70fcf1c2d0a4a979adfe44cebc93c20.html "Exchange user ID information between systems or environments in SAP BTP.") :arrow_upper_right:

-    [Connectivity](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e54cc8fbbb571014beb5caaf6aa31280.html) 

-   [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html)




<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_jm5_1nw_jgb"/>

## Identity Management and Authorization Management

Restrict access to any endpoint of your application through authentication and authorization. Identity and authorization management ensures that only the intended target group, such as your company's employees, can access your application. We recommend that you use SAML or OpenID Connect single sign-on protocol for user access and principal propagation for back-end access. If only access for technical users is needed, however, principal propagation isn't necessary. Once a user is authenticated, single sign-on propagates the credentials to the back-end system without requiring the user to reauthenticate.

Subaccounts get their users from identity providers. Administrators ensure that users can access only their subaccounts by establishing a dedicated trust relationship between the identity providers and the respective subaccounts. The preconfigured default identity provider for SAP BTP is SAP ID service. If you have an SAP Universal ID, you can log on with that service. You can also connect your own identity provider, which means you have full control over your user base.

> ### Recommendation:  
> For developing and administrating your own applications on SAP BTP, we recommend that you use [SAP Cloud Identity Services - Identity Authentication](https://help.sap.com/viewer/p/IDENTITY_AUTHENTICATION) as a hub, especially if your business users are stored in multiple corporate identity providers. Identity Authentication is SAP's cloud solution for identity lifecycle management for SAP BTP applications, and optionally for on-premise applications.

See the following for more information about security best practices:

-   [Setting Up Authentication](setting-up-authentication-1dbce9c.md)
-   [Setting Up Authorization](setting-up-authorization-cb9f0ac.md)
-   [Setting Up Identity Propagation](setting-up-identity-propagation-12cf719.md)



<a name="loio951d36ce07324f919f74f52b0f9f9e0a__section_ex2_25n_cgb"/>

## Security Considerations for Applications

When building applications, use the security features of SAP BTP, such as protection from web attacks. We recommend that your developers configure and deploy application-based security artifacts containing authorizations, and administrators assign these authorizations using the cockpit. SAP BTP offers platform roles that help you ensure a segregation of duties, such as between app development and administration.

It's likely that data protection and privacy influence your architecture and the functions of your application. Consider any implications as early as possible in your development process. Security monitoring is done with audit logging. SAP BTP writes logs for security-relevant events and the written log files are digitally signed to ensure their integrity.

See the following for more information about security best practices:

-   [Protection from Web Attacks](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/52750a8f86bb428ca224daa4312d122e.html "To protect your applications from different kind of web attacks, Neo environment provides mechanisms for you to use with your applications.") :arrow_upper_right:

-   [Giving Access Rights to Platform Users](giving-access-rights-to-platform-users-a03d08e.md)
-   [Data Protection and Privacy](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html "Data protection is associated with numerous legal requirements and privacy concerns. In addition to compliance with general data protection and privacy acts, it is necessary to consider compliance with industry-specific legislation in different countries.") :arrow_upper_right:


