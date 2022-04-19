<!-- loio40aa23277c7346a0a68de2f4c8b73e1c -->

# Extending Existing SAP Solutions Using SAP BTP

SAP BTP offers services, tools, and capabilities to develop, extend, or integrate business applications in the cloud. You can implement additional workflows or modules on top of existing solutions, which lets you benefit from out-of-the-box security, inherited data access governance, user interface embedding, and so on.



<a name="loio40aa23277c7346a0a68de2f4c8b73e1c__section_cl5_p4h_q3b"/>

## Overview

All standard SAP solutions are offered with customizing capabilities. Additionally, customers often have their own requirements for innovative or industry-specific extensions and the extension capability of SAP BTP can help them build, deploy, and operate their new functionalities easily and securely.

You can use SAP BTP to extend standard SAP solutions without disrupting their performance and core processes. When building extension applications, you can also benefit from the automation of the integration between and the SAP BTPextended SAP solutions.



### Extensions with Automated Configurations

SAP BTP provides a standard way for extending SAP solutions and developing event-driven extensions and applications. This framework includes:

-   Simplified, standardized and unified extensibility and configuration for the SAP solutions.

-   Central catalog per customer for all connected SAP systems where data such as APIs, events, credentials and other is stored. You can benefit from business services and actionable events across end-to-end business processes.


If you have to group the systems of different SAP solutions in the same business case, you can set up the connectivity between all these systems and SAP BTP in a single formation.

The following SAP solutions currently support the automated configurations:

-   SAP S/4HANA Cloud

-   SAP SuccessFactors

-   SAP Cloud for Customer

-   SAP Commerce Cloud

-   SAP Field Service Management




### Extensions with Manual Configurations

If the automated integration with SAP BTP does not support your scenario, you can configure the integration manually. Using manual configurations, you can extend SAP solutions on SAP BTP, such as:

-   SAP S/4HANA Cloud

-   SAP SuccessFactors

-   SAP Cloud for Customer




<a name="loio40aa23277c7346a0a68de2f4c8b73e1c__section_eyz_df1_xmb"/>

## Use Cases

The extension use cases include but are not limited to:

-   Extending the user interface of your SAP cloud solution.

    You can complement an existing SAP solution with a new or improved SAP Fiori user interface without adding any major logic or data.

    You can also provide necessary information and tools on mobile devices.

    For example:

    -   Building completely new user interfaces that can be seamlessly integrated in the SAP SuccessFactors Employee Central home page.

    -   Adding new functionality to SAP SuccessFactors by connecting it to other SAP solutions, such as SAP Commerce Cloud, SAP Cloud for Customer, SAP Field Service Management, SAP S/4HANA Cloud.

    -   Building completely new Fiori-based user interfaces that can be seamlessly integrated in the SAP Fiori launchpad.


-   Enhancing the functionality of your SAP cloud solution by connecting it with other SAP solutions.

    For example:

    -   Connecting SAP S/4HANA Cloud with other SAP solutions, such as SAP Commerce Cloud, SAP Cloud for Customer, SAP Field Service Management, SAP SuccessFactors.

    -   Connecting SAP SuccessFactors by connecting it to other SAP solutions, such as SAP Commerce Cloud, SAP Cloud for Customer, SAP Field Service Management, SAP S/4HANA Cloud.


-   Enhancing core business processes with analytics and machine learning capabilities.

-   Extend data insights by consolidating and combining data in one central place.

-   Building an extensions ecosystem, by creating and operating SaaS applications and selling them to multiple customers.

    For example, as an SAP Partner, you can build a multi-tenant SaaS extension application and provide it to your customers via:

    -   SAP App Center

    -   SAP BTP cockpit



For more use cases, see [https://www.sap.com/products/cloud-platform/use-cases.html?sort=title\_asc](https://www.sap.com/products/cloud-platform/use-cases.html?sort=title_asc).



<a name="loio40aa23277c7346a0a68de2f4c8b73e1c__section_i5q_521_xmb"/>

## Resources

The following resources are available for your extension scenarios. The links to various documents guide you through the configuration tasks that you need to perform to enable the SAP BTP for developing extension applications for your existing SAP solutions, and the learning journeys are collections of links to additional resources.

-   SAP S/4HANA Cloud

    -   [Extending SAP S/4HANA Cloud in the Cloud Foundry and Kyma Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/40b9e6c3cc43498b92472da13e88c7bf.html) \(SAP Help Portal\)

    -   [Extend SAP S/4HANA Cloud on SAP Business Technology Platform](https://discovery-center.cloud.sap/missiondetail/3277/3331) \(Mission in Discovery Center\)

    -   [Build an Event-Driven Geomarketing Extension for SAP S/4HANA Cloud](https://discovery-center.cloud.sap/missiondetail/3156/3192) \(Mission in Discovery Center\)

    -   [SAP Extensibility Explorer for SAP S/4HANA Cloud](https://extensibilityexplorer.cfapps.eu10.hana.ondemand.com/ExtensibilityExplorer/)

    -   [Tutorials about the integration of SAP BTP ABAP Environment with SAP S/4HANA Cloud](https://blogs.sap.com/2021/05/12/integrating-the-abap-environment-with-sap-s-4hana-cloud-hands-on-video-tutorials/)

    -   [SAP S/4HANA Cloud Extensions on SAP BTP](https://help.sap.com/doc/221f8f84afef43d29ad37ef2af0c4adf/HP_2.0/en-US/bd051afa72a745d49ce91344ad8f2628.html?collapse=) \(Learning Journey on SAP Help Portal\)

    -   [Extending SAP S/4HANA Cloud in the Cloud Foundry Environment Manually](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/6b9c4be039914ff2b3ff8b6669a9cadf.html) \(SAP Help Portal\)

-   SAP Customer Experience \(CX\) products

    -   [Extending SAP Customer Experience Products in the Kyma Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/83df31ad3b634c0783ced522107d2e73.html) \(SAP Help Portal\)

    -   [Create Extensions in the Kyma Environment Using Functions](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/fe4ba5b46f794037a4aee13df9df2d3c.html) \(SAP Help Portal\)

    -   [Extending SAP Cloud for Customer in the Cloud Foundry Environment Manually](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1150e4395ba6487bad2a7164db7ea417.html) \(SAP Help Portal\)


-   SAP SuccessFactors

    -   [Extending SAP SuccessFactors in the Cloud Foundry and Kyma Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/9e33934540c44681817567d6072effb2.html) \(SAP Help Portal\)

    -   [Extend SAP SuccessFactors on SAP BTP ](https://discovery-center.cloud.sap/missiondetail/3264/3309) \(Mission in Discovery Center\)

    -   [Build Resilient Cloud Native Applications](https://discovery-center.cloud.sap/missiondetail/3197/3228) \(Mission in Discovery Center\)

    -   [SAP SuccessFactors Extensions on SAP BTP](https://help.sap.com/doc/221f8f84afef43d29ad37ef2af0c4adf/HP_2.0/en-US/ba16ffc927ce4c26ad21b6c2b91fe38d.html) \(Learning Journey on SAP Help Portal\)



**Related Information**  


[Extensions](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Validation/en-US/08b1effc53634890a525f945017e2edc.html "The extension capabilities of SAP Business Technology Platform (SAP BTP) enables developers to implement loosely coupled extension applications securely, thus implementing additional workflows or modules on top of the existing SAP cloud solution they already have.") :arrow_upper_right:

