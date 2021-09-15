<!-- loio84ddc25bf6024506b9c56fbbe4438169 -->

# Integrate and Test

Test and integrate your application with other solutions.

 

 <a name="loio84ddc25bf6024506b9c56fbbe4438169 loiof0cc091b8e154132a84b449bd19adb0b__loiof0cc091b8e154132a84b449bd19adb0b"/>

<!-- loiof0cc091b8e154132a84b449bd19adb0b -->

# Integrating Your Application

SAP BTP offers various options for integrating your cloud application with other cloud and on-premise solutions.



<a name="loio84ddc25bf6024506b9c56fbbe4438169 loiof0cc091b8e154132a84b449bd19adb0b__section_i4b_fd3_r2b"/>

## Cloud Connector

If you want an application running on SAP BTP to access data from your on-premise back-end system, we recommend that you use the Cloud Connector. It's an on-premise piece of software that you'll need to install in your on-premise landscape, within the firewall. Once it's configured and paired with your SAP BTP subaccount, a secure tunnel is established between SAP BTP \(and all the services and applications that run on it\) and the Cloud Connector. Communication between SAP BTP and the back-end system is routed via the Cloud Connector through a secure SSL tunnel.

We recommend that you use the Cloud Connector if your use case requires any of the following:

-   Point-to-point connectivity and programmatic integration
-   Connectivity with cloud applications from on-premise systems, without mediation, such as for mapping, routing, or security
-   Data replication from on-premise databases or Business Intelligence tools to SAP HANA databases running in the cloud
-   On-premise system integration using SAP Cloud Integration

For more information, see [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Dev/en-US/e6c7616abb5710148cfcf3e75d96d596.html "Learn more about the Cloud Connector: features, scenarios and setup.") :arrow_upper_right:.



<a name="loio84ddc25bf6024506b9c56fbbe4438169 loiof0cc091b8e154132a84b449bd19adb0b__section_yy5_4h3_r2b"/>

## SAP Cloud Integration

SAP Cloud Integration \(Cloud Integration\) supports end-to-end process integration across cloud and on-premise applications \(cloud to cloud and cloud to on-premise integration\). It provides the following features:

-   Core runtime for processing, transforming, and routing of messages to be exchanged between your systems

-   Out-of-the-box connectivity support \(IDoc, SFTP, SOAP/HTTPS, SAP SuccessFactors, OData, HTTPS\)
-   Security features such as content encryption and certificate-based communication

Cloud Integration offers full flexibility for the manner in which messages are exchanged between your systems. We recommend that you use the Cloud Connector if you require any of the following \(or if you don't require on-premise-based middleware, such as SAP Process Orchestration\):

-   Compliance scenarios, such as e-invoicing and payroll
-   Graphical model of integration flow
-   More than a few systems to be integrated, and you'd like to managed integrations centrally, rather than having to manually code applications when connections change
-   Individual messages to be processed during integration
-   Integration with third-party solutions

For more information, see [SAP Cloud Integration](https://help.sap.com/viewer/product/CLOUD_INTEGRATION/Cloud/en-US).



<a name="loio84ddc25bf6024506b9c56fbbe4438169 loiof0cc091b8e154132a84b449bd19adb0b__section_c1v_rc3_r2b"/>

## Cloud Integration Automation Service

If you're planning on integrating your SAP BTP application into a hybrid landscape, you can also leverage the Cloud Integration Automation Service that is offered for selected integration scenarios. This service provides a guided workflow that uses customer-specific system information, reusable configuration settings between tasks, and automated execution capabilities, thereby reducing the manual work for your scenario integration. For more information, see [Cloud Integration Automation Service](https://help.sap.com/viewer/p/Cloud%20Integration%20Automation%20Service).

**Related Information**  


[Blog Post: SAP Cloud Integration: When to use which tool](https://blogs.sap.com/2016/04/29/sap-hana-cloud-platform-integration-services-when-to-use-which-tool/)

[Blog Post: Using SAP Analytics Cloud Connector with SAP Cloud Integration](https://blogs.sap.com/2017/04/14/using-sap-cloud-platform-cloud-connector-with-sap-cloud-platform-integration/)

[Blog Post: Cloud Integration Automation Service - What is it?](https://blogs.sap.com/2018/05/28/cloud-integration-automation-service-what-is-it/)

[Blog Post: Cloud Integration Automation Service: Step-by-Step](https://blogs.sap.com/2018/06/08/cloud-integration-automation-service-step-by-step/)

 <a name="loio84ddc25bf6024506b9c56fbbe4438169 loio998fbbb1a53c4fbb888e9b14892b3c0c__loio998fbbb1a53c4fbb888e9b14892b3c0c"/>

<!-- loio998fbbb1a53c4fbb888e9b14892b3c0c -->

# Performing Integration Tests

In contrast to unit tests that are performed locally on your development subaccount without any external dependencies in the develop and build phase, integration tests target the interplay of a complete system, spanning several single components and units potentially spread throughout a hybrid landscape. Integration tests verify that all building blocks work together, meet specified requirements, and fulfill the targeted business case. They should therefore then be executed on your test infrastructure or in your test subaccount after the integration into an existing landscape has taken place. This ensures that the interplay with backend functionalities is verified. In a CI/CD setup, note that such integration tests are part of the pipeline.



<a name="loio84ddc25bf6024506b9c56fbbe4438169 loio998fbbb1a53c4fbb888e9b14892b3c0c__section_cfw_qtc_wgb"/>

## Integration Tests for SAPUI5

One Page Acceptance Tests \(OPA5\) is an API for SAPUI5 controls. It hides asynchronicity and eases access to SAPUI5 elements. This makes OPA especially helpful for testing user interactions, integration with SAPUI5, navigation, and data binding. See [Integration Testing with One Page Acceptance Tests \(OPA5\)](https://help.sap.com/doc/saphelp_uiaddon20/2.05/en-US/7c/dee404cac441888539ed7bfe076e57/frameset.htm).



<a name="loio84ddc25bf6024506b9c56fbbe4438169 loio998fbbb1a53c4fbb888e9b14892b3c0c__section_fbq_ync_wgb"/>

## Integration Tests for Apps Written Using SAP Cloud SDK

Integration tests work directly on the defined backend APIs, mainly testing the integration between backend services and the integration between SAP BTP to SAP S/4HANA systems. For integration tests of your backend services, we recommend that you use Arquillian to spawn a server that contains only the resources for the specific backend services that you want to test. See [Step 13 with SAP Cloud SDK: Automated Testing](https://blogs.sap.com/2017/09/19/step-12-with-sap-s4hana-cloud-sdk-automated-testing/).

