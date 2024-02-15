<!-- loio13359fede8e0422e885d86fbea3a3c38 -->

# Example: Deliver a Multi-Target Application using Continuous Integration and Transport Management

When developing applications for SAP BTP, you can combine the agility of Continuous Integration with the control of Transport Management.

You create the application with the IDE of your choice for example SAP Business Application Studio. The artefacts are stored in a central source code repository. Whenever a developer commits a change to the source code repository a continuous integration pipeline starts. For typical SAP BTP scenarios, such as development with SAP Cloud Application Programming Model, we recommend using the SAP Continuous Integration and Delivery Service. The pipeline templates contain steps to build the application, run automated tests and deploy the application to your development subaccount.

It is also possible to handover the MTA to SAP Cloud Transport Management in the release stage of the pipeline. This creates a transport request which can then be handled according to your governance requirements. We recommend initiating this step only for qualified release candidates of your application. This can be achieved for example by using a separate release pipeline.

Optionally, SAP Cloud Transport Management can be integrated with SAP Cloud ALM or SAP Solution Manager. With that you can manage hybrid projects, including SAP BTP and on-premise parts.

**Related Information**  


[Continuous Integration and Delivery Best Practices Guide](https://help.sap.com/docs/CICD_OVERVIEW/3324745951b44b578bd65221d2ff8f9a/1ae37c7c7ad343589e2bd2fd424c9105.html)

[Transporting Multitarget Applications with CTS+](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/f598f69a9be347029b7e5e7205fc7d1f.html "You can enable transport of SAP BTP applications and application content that is available as Multitarget Applications (MTA) using the Enhanced Change and Transport System (CTS+).") :arrow_upper_right:

