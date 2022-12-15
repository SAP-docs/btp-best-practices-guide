<!-- loiob1b929a5aea64571b2f74e810b622568 -->

# Develop Resilient Applications

Our best practices about resilient application design help you to make your applications running on SAP BTP stable and highly available.



There are many different principles and patterns you can use to make your software resilient. It is, however, not always easy to find the combination that best fits your applications. The *Developing Resilient Apps on SAP BTP* guide gives an overview of the various options you have when developing applications and detailed information about the individual patterns you can use. Have a look at examples for applied resilience principles and find out how to develop your own resilient apps on SAP BTP: **[Developing Resilient Apps on SAP BTP](https://help.sap.com/viewer/eadaa45871804b4a974be865f627e791/Cloud/en-US/d1fe5fd8ecfb46c193221ebb991af3d7.html)**.



<a name="loiob1b929a5aea64571b2f74e810b622568__section_developaz"/>

## Developing Resilient Applications in the Cloud Foundry Environment

In the Cloud Foundry environment, you can make use of the availability zones \(AZ\): Benefit from the high availability mechanisms in Cloud Foundry by setting up your applications with multiple instances. You do not have to do anything explicitly to distribute the instances across the different AZs - this is handled by the platform.

Setting up your application with multiple instances might have an impact on your applications' capability for handling requests: In case of an AZ failure in a 3-AZ-deployment, at least one third of the application instances are affected and unavailable until Cloud Foundry can reschedule these instances on a healthy virtual machine.

   
  
**Distribution During an Availability Zone Failure**

 ![](images/AZ_failure_3e96947.png "Distribution During an Availability Zone Failure") 

During that period, the remaining instances in the healthy AZs have to carry the request load.

For more information about availability zones, see [Availability Zones in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/9c7092c7b7ae4d49bc8ae35fdd0e0b18.html#loiob6a7e11c3a58416a9ab1175bba17193a "The Cloud Foundry environment follows the recommendations of our partner IaaS providers by leveraging the availability zones (AZ) concept.") :arrow_upper_right:.



See also:

-   [Resilience, High Availability, and Disaster Recovery](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/e3ac4f7c25a3442ca585950095eec599.html#loioe3ac4f7c25a3442ca585950095eec599 "SAP has a number of processes in place to support resilience in SAP BTP, and provides different offerings so that you can support the high availability of your applications.") :arrow_upper_right: \(Cloud Foundry, ABAP and Kyma Environments\)

-   [Resilience, High Availability, and Disaster Recovery](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/84dd155500224fe4a7f161d48ee226a9.html "SAP has a number of processes in place to support resilience in SAP BTP, and provides different offerings so that you can support the high availability of your applications.") :arrow_upper_right: \(Neo Environment\)


