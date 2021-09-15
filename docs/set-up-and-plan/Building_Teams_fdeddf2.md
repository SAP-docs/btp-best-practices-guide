<!-- loiofdeddf22a6964d86a199b9eb11c7075e -->

# Building Teams

We recommend that you set up two types of teams: **Cloud Development Teams**, who build and operate applications, and a central **Cloud Administration Team / Center of Excellence**, who is responsible for any account operations, the build infrastructure, for defining central governance and compliance guidelines, and for driving cloud adoption throughout your organization.

 <a name="loiofdeddf22a6964d86a199b9eb11c7075e loiof36d159b91004ebda56faf35c2ebd90d__loiof36d159b91004ebda56faf35c2ebd90d"/>

<!-- loiof36d159b91004ebda56faf35c2ebd90d -->

# Cloud Administration Team / Center of Excellence

The Cloud Administration Team defines, sets up, and maintains your cloud landscape.

The responsibility of this team is to operate and ensure a stable and secure cloud landscape, and to enable other developers to build cloud applications. The members of this team are highly qualified experts who have development experience and experience with setting up and running a build infrastructure for continuous deployments and integration scenarios.

This team can support your development teams by providing knowledge and defining guidelines that match your company’s quality and security requirements. The Cloud Administration Team should generally not be responsible for the lifecycle management of specific applications; the Cloud Development Team should take responsibility for this task.

The Cloud Administration Team can also operate as a Center of Excellence \(CoE\), driving cloud adoption, migration, and operation throughout your organization by providing thought leadership and guidance for resolving roadblocks. The CoE is also responsible for identifying, evaluating, and implementing use cases for the SAP BTP.

We recommend that the Cloud Administration Team / Center of Excellence \(CoE\) create the following documents:

-   [Onboarding Document](Creating_an_Onboarding_Process_for_Development_Projects_4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_onboarding_doc)

-   [Security Document](Creating_an_Onboarding_Process_for_Development_Projects_4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_security_doc)

-   [Services Catalog](Creating_an_Onboarding_Process_for_Development_Projects_4bd29a8.md#loio4bd29a8a49c84727aeb81a8f60e74ea0__section_services_catalog)


 <a name="loiofdeddf22a6964d86a199b9eb11c7075e loio4157200ef2644243aa74ae2770df1d94__loio4157200ef2644243aa74ae2770df1d94"/>

<!-- loio4157200ef2644243aa74ae2770df1d94 -->

# Cloud Development Teams

The Cloud Development Teams are responsible for developing and operating the applications that run on SAP BTP.

Teams that develop on-premise applications often follow a Build-Run setup. The Build team develops the application, then passes it to the Run team, which operates and maintains it. However, this setup is not optimal in a cloud application development environment.

We recommend that Cloud Development Teams follow a DevOps approach, which means that the team both develops**and** operates applications. The team should maintain applications regularly after Go Live, and fix any issues. For example, if the team develops an SAPUI5 front end, they should verify at least every six months that the UI controls used are still supported by the latest SAPUI5 version. This doesn't require much effort, but does need to be checked to ensure the application continues running properly.

