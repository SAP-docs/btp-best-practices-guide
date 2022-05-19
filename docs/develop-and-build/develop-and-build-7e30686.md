<!-- loio7e306865dadb4473a4d66d81b7d83004 -->

# Develop and Build

SAP BTP offers various tools and programming languages for application development. You might also want to consider to integrate your application with other solutions.

We recommend that you use the SAP Cloud Application Programming Model for your development projects. For more information, see [Cloud Application Programming Model](cloud-application-programming-model-042061d.md).

Depending on your use case and the skill set of your developers, you can choose the runtime environment of your choice:

<a name="loio7e306865dadb4473a4d66d81b7d83004__table_jsf_jmx_l4b"/>Environment options


<table>
<tr>
<th valign="top">

 



</th>
<th valign="top">

Cloud Foundry



</th>
<th valign="top">

Kyma



</th>
<th valign="top">

ABAP



</th>
</tr>
<tr>
<td valign="top">

**Benefits**



</td>
<td valign="top">

-   Simplified developer experience for business application development
-   Large choice of programming languages
-   Intuitive “code-to-container” packaging and deployment, managed by the platform
-   Platform-managed application security patching and updates
-   Automatic application routing, load balancing, health checks, and multilevel self-healing
-   Support for CAP – an opinionated business app development framework



</td>
<td valign="top">

-   Free choice of programming languages and models \(containerized deployments\)
-   Combines microservices and serverless functions
-   Brings built-in, managed, service mesh
-   More flexible with Kubernetes
-   Support for CAP – an opinionated business app development framework



</td>
<td valign="top">

-   ABAP programming language
-   Fast prototyping with ABAP RESTful Programming Model \(RAP\)
-   Integrated development lifecycle
-   Reuse existing on-prem ABAP assets



</td>
</tr>
<tr>
<td valign="top">

**Shared Benefits**



</td>
<td valign="top" colspan="3">

-   No infrastructure vendor lock-in

-   Build scalable multitenancy business applications \(SaaS\)

-   Out-of-the-box consumption of SAP and hyperscaler services

-   Built on industry standards and open technology




</td>
</tr>
<tr>
<td valign="top">

**Good For**



</td>
<td valign="top">

-   Managed build-on approach
-   Enterprise-grade business applications and services
-   Cloud-native web applications and services
-   Scalable, microservice-based applications
-   Small to medium extensions built with CAP/low-code tooling



</td>
<td valign="top">

-   Open build-on approach
-   Cloud-native development of apps and services
-   Highly scalable, microservice-based applications
-   Applications built with CAP



</td>
<td valign="top">

-   User-centric process extensions
-   Robust, transactional cloud applications
-   Migrating and adapting add-ons to the cloud
-   Reusing existing on-premise ABAP code
-   Enabling ABAP developers to go to the cloud



</td>
</tr>
<tr>
<td valign="top">

**Skills**



</td>
<td valign="top">

-   Any major programming languages
-   SAP Fiori/UI5 and SAP HANA



</td>
<td valign="top">

-   Kubernetes knowledge
-   Docker
-   NodeJS or Python for serverless functions
-   Any major programming language
-   SAP Fiori/UI5 and SAP HANA



</td>
<td valign="top">

-   Ability to write modern ABAP code
-   Core data services
-   SAP Fiori/UI5 and SAP HANA



</td>
</tr>
</table>



We recommend that you create multitarget applications for managing dependencies more easily. For more information, see [Using Multitarget Applications to Manage Dependencies](using-multitarget-applications-to-manage-dependencies-41184aa.md).

For best practices, guidelines and step-by-step instructions, see [Development](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/c2fec62b49fa43b8bd945c85ecc2e5bd.html "Develop and run business applications on SAP Business Technology Platform (SAP BTP) using our cloud application programming model, APIs, services, tools, and capabilities.") :arrow_upper_right:.

If you need information about the Neo environment, please have a look at [Development, Neo Environment.](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/4543511443c640da94f2850f8f73dda2.html)



<a name="loio7e306865dadb4473a4d66d81b7d83004__section_fnv_kb3_r2b"/>

## Defining Development Guidelines

To ensure consistency and foster collaboration between developers, we recommend that you define guidelines that include standards for programming principles, code styles, and naming conventions.

SAP provides the following official guidelines:

-   [SAPUI5 Guidelines](https://sapui5.netweaver.ondemand.com/sdk/#/topic)

-   [SAP Fiori Design Guidelines](https://experience.sap.com/fiori-design/)

