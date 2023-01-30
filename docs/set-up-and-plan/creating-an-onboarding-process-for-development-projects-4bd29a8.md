<!-- loio4bd29a8a49c84727aeb81a8f60e74ea0 -->

# Creating an Onboarding Process for Development Projects

If you're planning on starting multiple development projects on SAP BTP, we recommend that you set up an onboarding process to ensure that new projects are tracked and documented properly, compliant with the security standards and guidelines you define.

Every new application that is managed and tracked by a Platform Engineering Team should have an onboarding process. Owners of new applications should fill out an onboarding document and a security template. Maintaining administrative information about all applications in one central place helps the Platform Engineering Team to keep an overview about all projects, applications, and responsibilities. It also allows the team to inform all project managers and developers about changes and updates to the cloud landscape.



<a name="loio4bd29a8a49c84727aeb81a8f60e74ea0__section_onboarding_doc"/>

## Onboarding Document

An onboarding document ensures that a new application is properly onboarded and documented. Onboarding can happen via e-mail, a ticketing system, or any other tool used in your company that you find suitable. The following provides an example of the information you might want to include:

-   Organization or department the application is being developed in
-   Application name
-   Technical application name \(only alphabetic characters, no spaces\)
-   Business case and application description
-   Planned Go-Live date
-   Application owners
-   Colleagues who need access to the development subaccount \(if you've set up a staged development environment\)
-   Whether the application will be accessible by external users
-   End-to-end data flow description, including connections to back-end systems
-   Programming languages and technologies that will be used
-   URL of the Git repository, if applicable
-   Test strategy

After the document is verified, application owners and developers should get access to the development subaccount to start developing. Make sure that all developers understand that on the development subaccount, all applications can be stopped, and code can be deleted by users at any time without notice. We recommend that the Cloud Development Team keeps the relevant code and files in a repository outside of SAP BTP to avoid that applications and artifacts like git repositories \(containing code\) are deleted in the subaccount by accident.



<a name="loio4bd29a8a49c84727aeb81a8f60e74ea0__section_security_doc"/>

## Security Document

We recommend you provide a template for the security document that is filled out for every new application, which is then approved by security experts in your company before you start developing. The template should ask for detailed information, such as:

-   Name of the application owners
-   Scenario description and business need
-   User groups, data classification, and confidentiality and integrity requirements
-   Compliance with any applicable security policies
-   End-to-end data flow
-   Data storage
-   Overview of all connected cloud and on-premise systems, used protocols, and ports
-   Authentication and high-level authorization concept
-   Auditing concept, logging, traceability



<a name="loio4bd29a8a49c84727aeb81a8f60e74ea0__section_services_catalog"/>

## Services Catalog

If you're going to onboard multiple development projects, we recommend that you set up a services catalog that summarizes all services offered by the Cloud Administration Team, especially when access to the testing and production subaccounts are restricted for developers. This facilitates and speeds up the collaboration between the Cloud Administration and the Cloud Development Teams. Examples of such services include the following:

-   Adding or managing destinations

-   Creating build plans
-   Restarting applications
-   Providing read access to the testing or production subaccounts
-   Creating database schemas and giving access to a specific schema

All services should be offered as templates in a service catalog that developers can fill out, for example, in a ticketing system.

We recommend that the Platform Engineering Team makes the consumption of services as easy as possible, or even automates it using SAP BTP APIs. The team may want to, for example, write scripts for database schema creation and access management. The Lifecycle Management API lets the Cloud Development Team restart an application in the production subaccount without having access to it and without affecting any other application. For more information, see the [Lifecycle Management API](https://api.sap.com/api/SAP_HCP_Lifecycle_Management/overview).

**Related Information**  


[API Documentation](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/4570e92cd29e419dbeee4caa1ef90701.html "API documentation for the Neo environment.") :arrow_upper_right:

