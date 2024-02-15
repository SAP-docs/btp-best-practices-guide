<!-- loio7e306865dadb4473a4d66d81b7d83004 -->

# Develop and Build

SAP BTP offers various tools and programming languages for application development. You might also want to consider to integrate your application with other solutions.

We recommend that you use the SAP Cloud Application Programming Model for your development projects. For more information, see [SAP Cloud Application Programming Model](sap-cloud-application-programming-model-042061d.md).

Depending on your use case and the skill set of your developers, you can choose the runtime environment of your choice:

**Environment options**


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
-   Built-in, managed, service mesh, and other cloud-native open-source modules to reduce the development effort
-   Managed infrastructure: day-2 operations, security patches, and updates
-   Refined horizontal and vertical automatic scalability
-   More flexible with Kubernetes
-   Dedicated application runtime
-   Zero downtime infrastructure setup by default
-   Support for CAP – an opinionated business app development framework
-   More flexible with Kubernetes



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

**Additional Information**

</td>
<td valign="top">

[Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/comparison-btp-runtimes/runtime-comparison?version=Cloud)

</td>
<td valign="top">

[Comparison: SAP BTP, Kyma Runtime and SAP BTP, Cloud Foundry Runtime](https://help.sap.com/docs/btp/comparison-btp-runtimes/runtime-comparison?version=Cloud)

</td>
<td valign="top">

[Development in the ABAP Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/development-in-abap-environment?version=Cloud)

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
-   Enterprise-grade applications
-   Cloud-native development of apps and services
-   Low latency infra-services communication
-   Reduced infrastructure management effort
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



Metering:

-   Cloud Foundry runtime: Metering starts when you start using the runtime memory, for example, when you deploy an application.

    If your global account uses the consumption-based commercial model and you want to understand how the consumption of SAP BTP, Cloud Foundry runtime is calculated, see[Consumption Monitoring](https://help.sap.com/docs/cf-runtime/cloud-foundry-runtime/monitoring-and-troubleshooting?version=Cloud) in the SAP BTP Cloud Foundry runtime documentation.

-   Kyma runtime: Metering starts when you enable the Kyma environment. This triggers the creation of a dedicated Kubernetes cluster, and the cluster is metered from the start, before you have deployed any applications.




For Cloud Foundry , we recommend that you create multitarget applications for managing dependencies more easily. For more information, see [Using Multitarget Applications to Manage Dependencies](using-multitarget-applications-to-manage-dependencies-41184aa.md).

For best practices, guidelines and step-by-step instructions, see [Development](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/c2fec62b49fa43b8bd945c85ecc2e5bd.html "Develop and run business applications on SAP Business Technology Platform (SAP BTP) using our cloud application programming model, APIs, services, tools, and capabilities.") :arrow_upper_right:.



<a name="loio7e306865dadb4473a4d66d81b7d83004__section_fnv_kb3_r2b"/>

## Defining Development Guidelines

To ensure consistency and foster collaboration between developers, we recommend that you define guidelines that include standards for programming principles, code styles, and naming conventions.

SAP provides the following official guidelines:

-   [SAPUI5 Guidelines](https://sapui5.netweaver.ondemand.com/sdk/#/topic)

-   [SAP Fiori Design Guidelines](https://experience.sap.com/fiori-design/)

