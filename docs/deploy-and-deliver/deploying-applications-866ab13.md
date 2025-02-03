<!-- loio866ab13d5f8e48cdaac6d70e55e76e09 -->

# Deploying Applications

For simple applications \(and if you don't have a need for governance and scalability\), you can use different manual deployment tools and methods, depending on your environment and your application.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09__section_yrm_k3x_m1c"/>

## Deploying Simple Applications in Cloud Foundry and Neo

> ### Recommendation:  
> We recommend to handle interdependencies in Cloud Foundry and Neo by archiving all components of your application into one package, which also includes a deployment descriptor. On SAP BTP, this package is called “multitarget application archive” \(MTA archive\).
> 
> For a manual process, you trigger the deployment of the solution manually, depending on your programming language. The SAP BTP deployment infrastructure automatically deploys the MTA files, considering all interdependencies specified in the MTA deployment descriptor that is part of the MTA archive.



### Deploying a Java application manually

For Java applications, you can use:

-   The SAP BTP cockpit

-   The Cloud Foundry command-line interface

-   The console client \(Neo\)


You can choose from several options with regards to runtimes, Java Virtual Machine versions, and more.



### Deploying an HTML5 application manually

For HTML5 applications, you can use:

-   The SAP Business Application Studio

-   The Cloud Foundry command-line interface

-   The SAP BTP cockpit




### Deploying a Node.js application manually

For Node.js applications \(in Cloud Foundry\), you can use:

-   The SAP Business Application Studio

-   The Cloud Foundry command-line interface




### Deploying an SAP HANA Extended Application Services, Advanced Model \(SAP HANA XSA\) application manually

For SAP HANA XSA applications \(in Cloud Foundry\), you can use:

-   The SAP HANA Deployment Infrastructure \(HDI\) from within SAP Business Application Studio

-   The Cloud Foundry command-line interface




### Bring Your Own Buildpack

In the SAP BTP, Cloud Foundry environment, you can use your own buildpack to create applications. The deployment of such an application depends on the buildpack-specific development and deployment infrastructure.



<a name="loio866ab13d5f8e48cdaac6d70e55e76e09__section_bdc_fcg_s1c"/>

## Deploying Simple Applications in Kyma

In the Kyma environment, you can use any technology of choice, such as Java, NodeJS, Python, Scala, .Net, or others. The only requirement is to package your application in a Linux Docker image. For creating a Docker image, you can use a standard [Dockerfile](https://docs.docker.com/reference/dockerfile/), or use a [Cloud Native Buildpack](https://buildpacks.io/).

> ### Recommendation:  
> For a productive setup, use automation tools such as SAP Continuous Integration and Delivery, with [Helm charts](https://helm.sh/docs/topics/charts/) for configurations. For details, see [Delivering Applications](delivering-applications-b39bae3.md#loiob39bae31d35d4d039431973116363d57).
> 
> For simple scenarios, you can consider manual deployments.



### Deploying a Java application manually

Package your Java application in a Docker image and deploy it to Kyma environment. For an example, see [Java-based extension with API exposed via Microgateway](https://github.com/SAP-samples/kyma-runtime-extension-samples/tree/main/sample-extension-java), which covers both approaches - with a Dockerfile, and with Cloud Native Buildpacks.



### Deploying an HTML5 application manually

Package your application in a Docker image and use a Kubernetes Job with a [HTML5 application deployer](https://www.npmjs.com/package/@sap/html5-app-deployer#enable-process-exit-after-upload).



### Deploying a Node.js application manually

Package your application in a Docker image and and deploy it to Kyma environment. For an example, see [HANA Cloud NodeJS API](https://github.com/SAP-samples/kyma-runtime-extension-samples/tree/main/hana-nodejs), which outlines the approach with a Dockerfile. Alternatively, you can also use Cloud Native Buildpacks.



### Bring Your Own Buildpack

In the Kyma environment, use [Cloud Native Buildpacks](https://buildpacks.io/). For details, see [Wishes come true - Cloud Native Buildpack Support in SAP Continuous Integration and Delivery!](https://community.sap.com/t5/technology-blogs-by-sap/wishes-come-true-cloud-native-buildpack-support-in-sap-continuous/ba-p/13578382)

**Related Information**  


[Deploying to the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/2a21055cc94b4a528a820f73e6fa7d69.html "Get an overview of available deployment options.") :arrow_upper_right:

[SAP Tutorials: Deploying to the Kyma environment](https://developers.sap.com/tutorial-navigator.html?search=kyma+deploy)

[Deploy Workloads in the Kyma Environment to Extend SAP Systems](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/fe4ba5b46f794037a4aee13df9df2d3c.html "Access the Kyma environment and start creating extensions for SAP systems.") :arrow_upper_right:

