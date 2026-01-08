<!-- loiofdeddf22a6964d86a199b9eb11c7075e -->

# Building Teams

We recommend that you set up different types of teams: besides **Cloud Development Teams**, who build and operate applications, set up a central **Platform Engineering Team** or **Center of Expertise \(CoE\)** that's responsible for any account operations, the build infrastructure, for defining central governance and compliance guidelines, and for driving cloud adoption throughout your organization.

Also, the Platform Engineering Team strives to improve the development experience and the operational efficiency, in order to reduce the cognitive load of the development teams.



<a name="loiofdeddf22a6964d86a199b9eb11c7075e__section_tks_ppd_pdc"/>

## Cloud Development Teams

The Cloud Development Teams are responsible for developing and operating the applications that run on SAP BTP.

Teams that develop on-premise applications often follow a Build-Run setup. The Build team develops the application, then passes it to the Run team, which operates and maintains it. However, this setup is not optimal in a cloud application development environment.

We recommend that Cloud Development Teams follow a DevOps approach, which means that the team both develops **and** operates applications. The team should maintain applications regularly after Go Live, and fix any issues. For example, if the team develops an SAPUI5 front end, they should verify at least every six months that the UI controls used are still supported by the latest SAPUI5 version. This doesn't require much effort, but does need to be checked to ensure the application continues running properly.



<a name="loiofdeddf22a6964d86a199b9eb11c7075e__section_ujc_qpd_pdc"/>

## Platform Engineering Team / Center of Expertise

The Platform Engineering Team defines, sets up, and maintains your cloud landscape.

The responsibility of this team is to operate and ensure a stable and secure cloud landscape \(including the internal developer platform\), and to enable other developers to build cloud applications with reduced cognitive load. The members of this team are highly qualified experts who have development experience and experience with setting up and running a build infrastructure for continuous deployments and integration scenarios.

This team can support your development teams by providing knowledge and defining guidelines that match your company’s quality and security requirements. The Platform Engineering Team should generally not be responsible for the lifecycle management of specific applications - the Cloud Development Team should take responsibility for this task.

The Platform Engineering Team can also operate as a Center of Expertise \(CoE\), driving cloud adoption, migration, and operation throughout your organization by providing thought leadership and guidance for resolving roadblocks. The CoE is also responsible for identifying, evaluating, and implementing use cases for the SAP BTP.

Platform Engineering Teams can be complemented by enabling teams, composed of specialists that help to bridge knowledge gaps of development teams, detect missing capabilities and come up with ideas what additional offerings could help to further reduce the cognitive load of the development teams. For more information, see [Key Concepts from Team Topologies](https://teamtopologies.com/key-concepts).

We recommend that the Platform Engineering Team / Center of Expertise \(CoE\) create the following documents:

-   [Onboarding Document](creating-an-onboarding-process-for-development-projects-4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_onboarding_doc)

-   [Security Document](creating-an-onboarding-process-for-development-projects-4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_security_doc)

-   [Services Catalog](creating-an-onboarding-process-for-development-projects-4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_services_catalog)


**Related Information**  


[SAP BTP Center of Expertise \(CoE\) Guide](https://help.sap.com/docs/sap_btp_guidance_framework/4b5ea626b38a490b85e8c4d060286b46/d960c25778d341cb9e1e77022e575561.html?locale=en-US)

