<!-- loio9d6553950f3249c2a4004d2e293b7cc7 -->

# Setting Up Access to Remote Systems

Use SAP Connectivity service to enable your SAP BTP applications to access remote services on the Internet or in your on-premise systems. For connecting to Internet services, we recommend that you use APIs with destinations, and for cloud-to-on-premise scenarios, we recommend that you use destinations and the Cloud Connector.

If you use destinations, you achieve a separation between the application and the configuration, which means it's easier to make configuration changes. And you can use the destinations to store credentials and certificates.

You can create destinations on two different levels:

-   Subaccount level
-   Service instance level

If a destination should be available for the entire subaccount, you can create it on subaccount level. If it is used for a specific scenario only, we recommend that you create it on service instance level. For security reasons, the rescpective access authorizations should be limited to a minimum for each level.

For more information, see:

-   [Using the Destinations Editor in the Cockpit](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/using-destinations-editor-in-cockpit?version=Cloud)
-   [Access the Destinations Editor](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/access-destinations-editor?version=Cloud)
-   [Multitenancy in the Connectivity Service](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/multitenancy-in-connectivity-service?state=DRAFT)

The Cloud Connector is a lightweight on-premise agent that establishes a tunnel for connecting your cloud applications to on-premise systems. The Cloud Connector acts as a reverse invoke between the on-premise network and SAP BTP. That means you don't need to open in-bound ports in the firewall for external access from the cloud. The Cloud Connector provides a fine-granular access control mechanism, supports multiple protocols, such as RFC and HTTP, and can forward the cloud user identity using principal propagation. It enables users to log on to on-premise systems without logging in again by forwarding their current identity from the cloud. You can configure the Cloud Connector directly from the subaccount in the SAP BTP cockpit.

For more information about connectivity in ABAP and Kyma environments, see:

-   [Communication Operations](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/ac9137dd683d4c23b79e281278c499bb.html "") :arrow_upper_right: for the ABAP environment

-   [Connectivity in the Kyma Environment](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/7501fbc9aebd4e3180eddec977ca288d.html "Find an overview of Connectivity components you can use for different purposes in the Kyma environment.") :arrow_upper_right:


**Related Information**  


[Principal Propagation](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f70fcf1c2d0a4a979adfe44cebc93c20.html "Exchange user ID information between systems or environments in SAP BTP.") :arrow_upper_right:

[SAP Connectivity service](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/e54cc8fbbb571014beb5caaf6aa31280.html)

[Cloud Connector](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/e6c7616abb5710148cfcf3e75d96d596.html)

