<!-- loio866ab13d5f8e48cdaac6d70e55e76e09 -->

# Deploying Applications

You can leverage different deployment tools and methods, depending on the application type and your requirements.

 <a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__loioe3b003d6734d4f41a069324f8ed6ea27"/>

<!-- loioe3b003d6734d4f41a069324f8ed6ea27 -->

# Deploying Simple Applications

If your application consists of only one module, there are different native options for deploying it, depending on the programming language you're using.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_zzq_scx_m2b"/>

## Java

You can use the SAP BTP cockpit, the console client \(Neo\), or the command-line tool \(Cloud Foundry\) to deploy a Java application. You have several options to choose from with regards to runtimes, Java Virtual Machine versions, and more.

For large-scale development setups, we recommend that you connect your own development infrastructure.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_alw_qfx_m2b"/>

## HTML5

You can deploy HTML5 applications from within the SAP Web IDE. In addition:

-   In the Neo environment, you can export and import your application via the SAP BTP cockpit.

-   In the Cloud Foundry environment, you can deploy your application using the Cloud Foundry command-line interface.




<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_jpb_xfx_m2b"/>

## Node.js

In the Cloud Foundry environment, you can deploy Node.js applications from within SAP Web IDE, or use the Cloud Foundry command-line interface.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_pd1_3hx_m2b"/>

## SAP HANA Extended Application Services, Classic Model \(SAP HANA XS\)

In the Neo environment, you can create a delivery unit as a .tgz file that contains all the artifacts for applications that are based on SAP HANA XS. You can import and export the application using SAP HANA administration tools, and open the application using the SAP BTP cockpit.

Please be aware that SAP HANA Extended Application Services, Classic Model has been deprecated – for more information, see [0002465027](https://launchpad.support.sap.com/#/notes/0002465).



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_sqp_vhx_m2b"/>

## SAP HANA Extended Application Services, Advanced Model \(SAP HANA XSA\)

In the Cloud Foundry environment, you can deploy applications based on SAP HANA XSA using the SAP HANA Deployment Infrastructure \(HDI\) from within SAP Web IDE. You can also deploy your application using the Cloud Foundry command-line interface.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loioe3b003d6734d4f41a069324f8ed6ea27__section_h15_d3x_m2b"/>

## Bring Your Own Buildpack

In the Cloud Foundry environment, you can use your own buildpack to create applications. The deployment of such an application depends on the buildpack-specific development and deployment infrastructure.

 <a name="loio866ab13d5f8e48cdaac6d70e55e76e09 loio47e40d941149489299af4d15a6064465__loio47e40d941149489299af4d15a6064465"/>

<!-- loio47e40d941149489299af4d15a6064465 -->

# Deploying Multitarget Applications

There are two options for deploying MTAs: Manually or managed.

-   **Manually:** You can archive all components of your application into one package that includes the deployment descriptor. You can then manually trigger the deployment of the solution using the SAP BTP cockpit or the Console Client. The actual deployment of the MTA files is then performed automatically by the SAP BTP deployment infrastructure, considering all interdependencies specified in the MTA deployment descriptor that is part of the MTA archive. By assigning roles and encapsulating the Console Client in a script, you can achieve a somewhat controlled release mechanism.

-   **Managed:** If you prefer a managed approach, you can deploy MTAs as part of a CI/CD approach or implement transport or change management processes for your SAP BTP apps, using enhanced Change and Transport \(CTS+\) for example. For more information, see [f598f69a9be347029b7e5e7205fc7d1f.md](f598f69a9be347029b7e5e7205fc7d1f.md).

