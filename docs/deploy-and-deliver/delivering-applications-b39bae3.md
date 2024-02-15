<!-- loiob39bae31d35d4d039431973116363d57 -->

# Delivering Applications

There are several options for propagating developed applications and application-specific content from one subaccount to another; for example, from your Development to your Testing and Production subaccounts.




<table>
<tr>
<th valign="top">

Delivery Option \(Tool Support and Automation Decreasing from Top to Bottom\)

</th>
<th valign="top">

Development content \(such as Java, HTML5, SAP HANA XSA\)

</th>
<th valign="top">

SAP Integration packages

</th>
<th valign="top">

Other app-specific content

</th>
<th valign="top">

SAP HANA XS

</th>
<th valign="top">

Portal Site

</th>
</tr>
<tr>
<td valign="top">

Continuous Integration and Delivery \(CI/CD\)

</td>
<td valign="top">

recommended

</td>
<td valign="top">

n/a

</td>
<td valign="top">

n/a

</td>
<td valign="top">

recommended for SAP HANA XSA

</td>
<td valign="top">

partly possible

</td>
</tr>
<tr>
<td valign="top">

SAP Cloud Transport Management service with the option to integrate into Change Management \(SAP Cloud ALM change and deployment management, and SAP Solution Manager Change Request Management and Quality Gate Management\)

</td>
<td valign="top">

recommended

</td>
<td valign="top">

recommended, but only possible as MTA

</td>
<td valign="top">

recommended

</td>
<td valign="top">

recommended

</td>
<td valign="top">

recommended, but only possible as MTA

</td>
</tr>
<tr>
<td valign="top">

CTS+ with the option to integrate into Change Management \(SAP Solution Manager Change Request Management and Quality Gate Management\)

</td>
<td valign="top">

recommended, but only possible as MTA

</td>
<td valign="top">

recommended, but only possible as MTA

</td>
<td valign="top">

n/a

</td>
<td valign="top">

recommended

</td>
<td valign="top">

recommended, but only possible as MTA

</td>
</tr>
<tr>
<td valign="top">

SAP HANA Application Lifecycle Management

</td>
<td valign="top">

n/a

</td>
<td valign="top">

n/a

</td>
<td valign="top">

n/a

</td>
<td valign="top">

recommended for SAP HANA XSC

</td>
<td valign="top">

n/a

</td>
</tr>
<tr>
<td valign="top">

Manually

</td>
<td valign="top">

possible

</td>
<td valign="top">

possible

</td>
<td valign="top">

recommended, but with app-specific procedures

</td>
<td valign="top">

possible

</td>
<td valign="top">

possible

</td>
</tr>
</table>



<a name="loiob39bae31d35d4d039431973116363d57__section_s12_tm1_dxb"/>

## Continuous Integration and Delivery

Choose your SAP solution for continuous integration and delivery \(CI/CD\).

SAP offers two main approaches for applying CI/CD in your software development. Depending on your expertise in CI/CD, the required level of flexibility, the infrastructure you bring \(or don’t bring\) along, and the desired level of support, choose one of the following options:

**SAP Solutions for Continuous Integration and Delivery**


<table>
<tr>
<th valign="top">

CI/CD Solution

</th>
<th valign="top">

Required Expertise in CI/CD

</th>
<th valign="top">

Level of Flexibility

</th>
<th valign="top">

Infrastructure

</th>
<th valign="top">

Support

</th>
</tr>
<tr>
<td valign="top">

**[SAP Continuous Integration and Delivery service](https://help.sap.com/docs/CONTINUOUS_DELIVERY)** 

</td>
<td valign="top">

Low

</td>
<td valign="top">

Medium

</td>
<td valign="top">

SAP Continuous Integration and Delivery is ready to use and doesn’t need a separate CI/CD infrastructure.

</td>
<td valign="top">

Support provided by SAP

</td>
</tr>
<tr>
<td valign="top">

**[Project "Piper"](https://sap.github.io/jenkins-library/)** \(complemented by [Continuous Integration and Delivery Best Practices Guide](https://help.sap.com/docs/CICD_OVERVIEW/3324745951b44b578bd65221d2ff8f9a/1ae37c7c7ad343589e2bd2fd424c9105.html) 

</td>
<td valign="top">

Medium - high

</td>
<td valign="top">

Medium - high

</td>
<td valign="top">

Project "Piper" is an open-source project that provides preconfigured Jenkins pipelines, which you can use in your own Jenkins infrastructure and adapt according to your needs, if necessary. Project "Piper" requires Jenkins as underlying CI/CD infrastructure. If you don’t have a Jenkins instance, yet, use the Cx Server to bootstrap a preconfigured one, or use the step library and the Continuous Integration and Delivery Best Practices Guide to build own pipelines on any CI/CD infrastructure. See [Getting Started with Project "Piper"](https://www.project-piper.io/guidedtour/).

</td>
<td valign="top">

Open Source community and SAP Community support \(no direct support by SAP\)

</td>
</tr>
</table>

So, with the golden path for SAP-specific scenarios, SAP Continuous Integration and Delivery service targets rather typical SAP customers and partners with an ABAP background that are transitioning into the cloud, while Project 'Piper' offers full flexibility for experienced users with their own CI/CD stack and a high level of expertise.

For more information, see [SAP Solutions for Continuous Integration and Delivery](https://help.sap.com/viewer/8cacec64ed854b2a88e9a0973e0f97a2/Cloud/en-US/e9fa320181124fa9808d4446a1bf69dd.html) and [Which SAP Solution for CI/CD Meets Your Needs?](https://help.sap.com/viewer/8cacec64ed854b2a88e9a0973e0f97a2/Cloud/en-US/e9fa320181124fa9808d4446a1bf69dd.html#loioa49d1ba1ecef4e9d96deffd127c4522d)



<a name="loiob39bae31d35d4d039431973116363d57__section_t12_tm1_dxb"/>

## Transport Management

If you want to have more control, especially when propagating changes towards your production environment, consider the following transport and change management options:

-   For cloud transports, also in hybrid landscapes: the **SAP Cloud Transport Management** service, which allows you to transport content archives, delivery units of SAP HANA XS classic model, and application-specific content, such as SAP Cloud Integration content, between different subaccounts. Such subaccounts might even reside in different global accounts, spread across different regions. This service is recommended to handle SAP BTP application-specific content, independent of whether it is provided as multitarget application \(MTA\) files or in other formats.

    For more information, see [What is SAP Cloud Transport Management](https://help.sap.com/viewer/7f7160ec0d8546c6b3eab72fb5ad6fd8/Cloud/en-US)

-   For on-premise focused scenarios, the enhanced Change and Transport System \(CTS+\), running in an on-premise ABAP system. Besides handling the transport of on-premise systems, CTS+ also lets you transport SAP BTP artifacts from one subaccount to another. However, this is only supported if the artifacts are packaged as multitarget application \(MTA\) archives. Note that no other SAP BTP content format is planned to be supported by CTS+. Therefore, consider CTS+ for SAP BTP content, if you have CTS+ already in use and only have to handle MTA-based content on SAP BTP \(today and in the future\).

    For more information, see [Transporting Multitarget Applications with CTS+](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/f598f69a9be347029b7e5e7205fc7d1f.html "You can enable transport of SAP BTP applications and application content that is available as Multitarget Applications (MTA) using the Enhanced Change and Transport System (CTS+).") :arrow_upper_right:

-   SAP Cloud Transport Management service does allow an integration into change and deployment management of SAP Cloud ALM. For more information, see [SAP Cloud Transport Management Service](https://help.sap.com/docs/cloud-alm/setup-administration/cloud-transport-management?locale=en-US)

-   For providing its service, SAP Cloud Transport Management works together with local agents, such as SAP Content Agent service in the SAP BTP Cloud Foundry runtime. SAP Content Agent service eases the local management of application-specific content by offering export/import and content assembly - interplaying with central transport and change management capabilities or used standalone via its own user interface. For more information, see [Introduction to SAP Content Agent Service](https://help.sap.com/docs/content-agent-service/user-guide/introduction?version=Cloud)
-   Both CTS+ and SAP Cloud Transport Management allow an integration into change management approaches around SAP Solution Manager. You can either run CTS+ centrally on SAP Solution Manager and integrate it with change management tools, such as Change Request Management or Quality Gate Management – or you can integrate SAP Cloud Transport Management service into these tools running on SAP Solution Manager \(minimum version: SAP Solution Manager 7.2 SP10\). It's even possible to use CTS+ and SAP Cloud Transport Management service in parallel within Change Request Management or Quality Gate Management.

-   With these approaches, you can set up synchronized transports in hybrid scenarios \(involving both on-premise ABAP content and SAP BTP content\). For more information, see [Interplay of SAP Transport Management, CTS+ and ChaRM in hybrid landscapes](https://blogs.sap.com/2020/01/31/interplay-of-sap-cloud-platform-transport-management-cts-and-charm-in-hybrid-landscapes/)




<a name="loiob39bae31d35d4d039431973116363d57__section_pql_1n1_dxb"/>

## CI/CD with Transport Management

Combine CI/CD with transport management \(either in the form of SAP Cloud Transport Management service or CTS+\), to gain more control over the delivery of release candidates towards your production environment and at the same time benefit from the agility CI/CD brings to your development. For more information, see [How to integrate SAP Transport Management into your CI/CD pipeline](https://blogs.sap.com/2019/08/20/how-to-integrate-sap-cloud-platform-transport-management-into-your-cicd-pipeline/). It's also possible to combine CI/CD, CTS+, SAP Cloud Transport Management, and change management. If you use SAP Continuous Integration and Delivery service, you can define an automated hand-over from your pipeline into SAP Cloud Transport Management out-of-the-box.



<a name="loiob39bae31d35d4d039431973116363d57__section_nbz_tn1_dxb"/>

## Manually

-   **Deploy applications manually** from your IDE to different subaccounts. Import or export your application using the SAP BTP cockpit, or use the Console Client for the Neo environment or the Cloud Foundry command line interface to deploy your application.

    > ### Note:  
    > You can transport portal settings and configurations only by manually redeploying your application in each subaccount.

-   In the Neo environment, consider to use the Solution Export Wizard that you can start in SAP BTP cockpit to model solutions by selecting comprised components \(with an automated resolution of interdependencies\) and to either export the outcome \(as multitarget application file\) or to directly handle the modeled solution using the change management options outlined above. For more information, see [Solution Export Wizard - Ease Modeling and Export of Solutions as MTA](https://blogs.sap.com/2018/08/03/solution-export-wizard-ease-modeling-and-export-of-solutions-as-mta/).

-   \(HTML5 applications only\) **Synchronize Git repositories** and create build scripts that let you transfer commits from the repository of the source subaccount to the repository of the target subaccount. After the synchronization, you must still deploy the application manually using the SAP BTP cockpit.
-   \(SAP HANA XS applications only\) Use the **SAP HANA XS Application Lifecycle Management \(HALM\)** to create transport routes between two SAP HANA systems, then transport delivery units between those systems. For more information, see [SAP HANA Application Lifecycle Management](https://help.sap.com/viewer/52715f71adba4aaeb480d946c742d1f6/2.0.03/en-US/9a012d6438764459a581e6af55a87c46.html).


**Related Information**  


[Blog on Transport Approaches in SAP BTP](https://blogs.sap.com/2017/06/30/part-6-transport-approaches-in-sap-cp/)

