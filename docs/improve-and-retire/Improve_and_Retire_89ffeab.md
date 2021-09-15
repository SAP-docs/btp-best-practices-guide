<!-- loio89ffeab7ea7742fd9a1ad2de4970b077 -->

# Improve and Retire

Once your application has gone live, we recommend that you continually ensure its quality. If you determine that you no longer need it, you should retire it.

 <a name="loio89ffeab7ea7742fd9a1ad2de4970b077 loio069ff72db3624ea3ba06582ad65e3996__loio069ff72db3624ea3ba06582ad65e3996"/>

<!-- loio069ff72db3624ea3ba06582ad65e3996 -->

# Improving and Maintaining Your Application

Once an application has gone live, the Cloud Development Team is responsible for housekeeping and ongoing improvements.

The team should:

-   Regularly verify and test the application to avoid issues caused by library and platform updates, such as a new SAPUI5 version
-   Ensure that the application remains compliant with all applicable standards and guidelines
-   Fix bugs in a timely manner, and ensure that the user experience remains of high quality and is improved and adapted over time
-   Listen to user feedback

-   Set up alerting that informs you automatically about issues with your application, for example by using [SAP Alert Notification Service](https://help.sap.com/viewer/product/ALERT_NOTIFICATION/Cloud)

-   Identify recurring operation tasks and automate them, such as by using [SAP Automation Pilot](https://help.sap.com/viewer/product/AUTOMATION_PILOT/Cloud/en-US). This services provides catalogs of automated technical operation tasks for handling the lifecycle of apps running on SAP BTP, such as for alert remediation and recurring DevOps tasks.

-   Adapt/extend your application, as required:

    -   For deploying new application versions in the Cloud Foundry environment, consider using a blue-green deployment, in which you deploy a new application version in parallel to the previous version to test it and to route to the new version only after successful testing and without downtime – for more information, see [Multitarget Application Commands for the Cloud Foundry Environment](https://help.sap.com/doc/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/65ddb1b51a0642148c6b468a759a8a2e.html) on SAP Help Portal.
    -   In the Cloud Foundry environment, consider using the Feature Flag service that lets you enable or disable specific features in a production solution, for testing purposes, without having to redeploy or restart the solution.


> ### Recommendation:  
> To stay up to date, we recommend that you regularly check the [Release Notes](https://help.sap.com/doc/43b304f99a8145809c78f292bfc0bc58/Cloud/en-US/98bf747111574187a7c76f8ced51cfeb.html) and the [SAP Community](https://www.sap.com/community/topic/cloud-platform.html).

 <a name="loio89ffeab7ea7742fd9a1ad2de4970b077 loio06deb3339dfa4b91aa8ed99a3018303d__loio06deb3339dfa4b91aa8ed99a3018303d"/>

<!-- loio06deb3339dfa4b91aa8ed99a3018303d -->

# Retiring Your Application

If your application is no longer needed, the Cloud Administration and the Cloud Development Teams should ensure that it is properly retired, and that all data retention requirements are met.

 <a name="loio89ffeab7ea7742fd9a1ad2de4970b077 loio13cbe434ce0a48bca14f1112f3db52b7__loio13cbe434ce0a48bca14f1112f3db52b7"/>

<!-- loio13cbe434ce0a48bca14f1112f3db52b7 -->

# Migrating from Neo to Multi-Cloud

SAP is integrating more closely with hyperscalers, such as Amazon Web Services, Google Cloud Platforrm, and Microsoft Azure. If you are currently running secnarios in our Neo enviroment, please have a look at our migration guide for moving from Neo to the multi-cloud foundation.

[Migrating from the Neo Environment to the Multi-Cloud Foundation (Cloud Foundry and Kyma)](https://help.sap.com/viewer/b017fc4f944e4eb5b31501b3d1b6a1f0/Dev/en-US/aae4e0ae1cdf434b908c3c8cf3ea942a.html "Learn why and how to migrate your scenarios on SAP Business Technology Platform (SAP BTP) from the Neo environment to the multi-cloud foundation.") :arrow_upper_right:

