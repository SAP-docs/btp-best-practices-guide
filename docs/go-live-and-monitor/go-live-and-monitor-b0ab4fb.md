<!-- loiob0ab4fb5cb914ee19923e4a8f020e868 -->

# Go Live and Monitor

Once you've deployed, transported, tested, and integrated your application, you can go live.

After you've released an application, you have to ensure that it's provided with the right performance and availability by monitoring its various parts – such as platform services, application parts, and databases. SAP BTP offers various native tools for monitoring and operating your application, optionally complemented by third-party offerings, in case you need deep monitoring of cloud-native applications.

For hybrid scenarios across the SAP portfolio, or if you already have an operations process in place, you can also integrate operation aspects of SAP BTP into strategic operation platforms \(such as SAP Solution Manager, SAP Focused Run of SAP Solution Manager, and SAP Cloud ALM\).

 <a name="loio85cd2c84ad3b4d2bb0229b7d97fd8c63"/>

<!-- loio85cd2c84ad3b4d2bb0229b7d97fd8c63 -->

## Monitoring a Hybrid Landscape

If you've integrated SAP BTP with your on-premise SAP landscape, you can use SAP Solution Manager, Focused Run for SAP Solution Manager, and, for more and more options and scenarios also SAP Cloud ALM to monitor and operate that hybrid landscape.

For example, the table below lists monitoring options offered by SAP Solution Manager.

<a name="loio85cd2c84ad3b4d2bb0229b7d97fd8c63__table_xzc_byq_p2b"/>


<table>
<tr>
<th valign="top">

Monitoring Option



</th>
<th valign="top">

Description



</th>
<th valign="top">

More Information



</th>
</tr>
<tr>
<td valign="top">

Integration Monitoring



</td>
<td valign="top">

Ensure reliable data exchange between your SAP on-premise system and SAP BTP. Includes process integration monitoring, interface and connection monitoring, and message flow monitoring.



</td>
<td valign="top">

 [Integration Monitoring](https://help.sap.com/viewer/82f6dd44db4e4518aad4dfce00116fcf/7.2.07/en-US/43a776536c11f663e10000000a4450e5.html) 



</td>
</tr>
<tr>
<td valign="top">

User Experience Monitoring



</td>
<td valign="top">

Simulate the behavior of users who access central servers at different locations to run business processes. Lets you monitor the availability of the systems, and connection performance, from the end-user perspective, in real time.



</td>
<td valign="top">

 [User Experience Monitoring](https://help.sap.com/viewer/82f6dd44db4e4518aad4dfce00116fcf/7.2.05/en-US/ef80f08c-5e3a-4c29-903b-8338c66c0b38.html) 



</td>
</tr>
<tr>
<td valign="top">

Trace Analysis



</td>
<td valign="top">

Trace the performance of SAP BTP applications. You can:

-   Trace requests to applications that are deployed on SAP BTP or running on your on-premise system

-   Trace application performance data, such as application and UI response times, and database calls
-   Trace request paths through inbound and outbound request points



</td>
<td valign="top">

[Trace Analysis](https://help.sap.com/viewer/82f6dd44db4e4518aad4dfce00116fcf/7.2.07/en-US/a56e3b810bd74f37b9468bc27f55f696.html)

[End-to-End Trace Analysis](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/a1e3101e108a4ca7a2a8c62654534ef8.html "Trace user actions with excessive execution time within a complex system landscape using the End-to-End (E2E) trace analysis.") :arrow_upper_right: \(Neo environment\)



</td>
</tr>
<tr>
<td valign="top">

Exception Management



</td>
<td valign="top">

Forward business-critical exceptions from SAP BTP to on-premise operations and:

-   Centrally retrieve and handle all single, cross-components, process flow-driven, and multistep exceptions.

-   Correlate, analyze, and process exceptions, and use predefined guided procedures to quickly handle errors.



</td>
<td valign="top">

 [Exception Management](https://help.sap.com/viewer/82f6dd44db4e4518aad4dfce00116fcf/7.2.07/en-US/42875d2bc609497fb73453bfc7f1e407.html) 



</td>
</tr>
</table>

See also [SAP Cloud ALM for operations](https://support.sap.com/en/alm/sap-cloud-alm/operations.html).

**Related Information**  


[Blog: Brief Overview of Hybrid Supportability Options for SAP BTP](https://blogs.sap.com/2018/02/02/brief-overview-of-hybrid-supportability-options-for-sap-cloud-platform/)

 <a name="loio318c3653da0f42c88bd7a1c38273f79e"/>

<!-- loio318c3653da0f42c88bd7a1c38273f79e -->

## Monitoring Applications and Services

There are various options you can use to monitor applications and services on SAP BTP, provided natively by the platform itself. Which of them you might use depends on the SAP BTP environments you work in.



<a name="loio318c3653da0f42c88bd7a1c38273f79e__section_jsb_jz3_p2b"/>

## Monitoring Applications in the Cloud Foundry Environment

In the Cloud Foundry environment, you can use the [SAP Application Logging service for SAP BTP](https://help.sap.com/viewer/ee8e8a203e024bbb8c8c2d03fce527dc/Cloud/en-US/68454d44ad41458788959485a24305e2.html) to access logs from your applications. You can also run the Cloud Foundry CLI command `cf logs` to show the recent logs for an application. For more information, see the Cloud Foundry documentation at [https://docs.cloudfoundry.org/devguide/deploy-apps/streaming-logs.html](https://docs.cloudfoundry.org/devguide/deploy-apps/streaming-logs.html).

> ### Note:  
> Container metrics in syslog drains are not currently logged by SAP BTP, but you can use the SAP Application Logging service to access container metrics of your applications.

You can also configure health checks that continually monitor the status of a running application. For more information, see [https://docs.cloudfoundry.org/devguide/deploy-apps/healthchecks.html](https://docs.cloudfoundry.org/devguide/deploy-apps/healthchecks.html).



<a name="loio318c3653da0f42c88bd7a1c38273f79e__section_cld_pdx_42b"/>

## Monitoring Applications in the Neo Environment

In the Neo environment, you can use the cockpit to monitor applications:

<a name="loio318c3653da0f42c88bd7a1c38273f79e__table_yzh_g3d_p2b"/>Monitoring Applications Using the Cockpit in the Neo Environment


<table>
<tr>
<th valign="top">

Application Type



</th>
<th valign="top">

Monitoring Options



</th>
<th valign="top">

More Information



</th>
</tr>
<tr>
<td valign="top">

Java applications



</td>
<td valign="top">

-   Application monitoring

-   Application performance statistics \(Beta\)
-   Custom JMX checks
-   Monitoring APIs



</td>
<td valign="top">

 [Managing Applications in the SAP BTP Cockpit](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/764f53e1cc9c4a50b2d0587ac82fdd7f.html "For an overview of the current status of the individual applications in your subaccount, use the cockpit. It provides key information in a summarized form and allows you to initiate actions, such as starting, stopping, and undeploying applications.") :arrow_upper_right: 



</td>
</tr>
<tr>
<td valign="top">

SAP HANA XS applications



</td>
<td valign="top">

-   Health statistics for SAP HANA database instances

-   Application availability checks
-   Email notifications



</td>
<td valign="top">

 [SAP HANA: Application Operations](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/6902b488768a4b13a75c8d9d50055fa2.html "") :arrow_upper_right: 



</td>
</tr>
<tr>
<td valign="top">

HTML5 applications



</td>
<td valign="top">

Log viewer collecting error messages



</td>
<td valign="top">

 [Using Logs in the Cockpit for HTML5 Applications](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/9f358860642c4ed283cd889a5bc42461.html "You can view logs on an HTML5 application running in your subaccount or on a subscription to an HTML application.") :arrow_upper_right: 



</td>
</tr>
</table>

You can also connect your Java applications to a **Dynatrace SaaS monitoring environment**. For more information, see [Agent Activation for Dynatrace](https://help.sap.com/viewer/p/DYNATRACE_AGENT_ACTIVATION).



<a name="loio318c3653da0f42c88bd7a1c38273f79e__section_dyj_n1j_p2b"/>

## Monitoring Platform and Service Availability

You can follow the availability of the platform at [SAP Trust Center](https://www.sap.com/about/trust-center/cloud-service-status.html). You can check:

-   the availability by service on the *SAP BTP* tile of the *Cloud Status* tab page;

-   the availability by region on the *Data Center* tab page.


To get notifications for updates and downtimes, subscribe at the [Cloud System Notification Subscriptions](https://support.sap.com/en/my-support/systems-installations/cac.html) application. Create a subscription by specifying Cloud Product, Cloud Service, and Notification Type. For more information, see [Cloud System Notification Subscriptions User Guide](https://support.sap.com/content/dam/support/en_us/library/ssp/my-support/systems-installations/cac/csns_user_guide.pdf).

In addition, you can get a personalized, at-a-glance view of additional SAP BTP offerings with [SAP Cloud Availability Center](https://support.sap.com/en/my-support/systems-installations/cloud-systems-installations.html#section), such as SAP BTP Integration.

There are additional monitoring tools and options available for certain SAP BTP services, such as the SAP BTP Identity Authentication service. Please refer to the respective service documentation for more details: [Solutions and Services](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7613d9ce711e1014839a8273b0e91070.html#loio7613d9ce711e1014839a8273b0e91070 "Consume the solutions and services by SAP BTP according to your preferred development environment and use cases.") :arrow_upper_right:.



<a name="loio318c3653da0f42c88bd7a1c38273f79e__section_kpd_cnj_wfb"/>

## Alerting

In addition to the general notifications mentioned above, Alert Notification for SAP BTP service lets you know instantly whenever there's an issue with your specific cloud application or its dependencies, no matter if your apps are running in the Neo or Cloud Foundry environment. You can subscribe to events coming from used SAP BTP services, from hyperscalers, from third-party tools such as Dynatrace, or you can create custom alerts for your apps. Furthermore, the notifications arrive via any channel of alert management you select, for example, email, some sort of corporate chat, a ticketing system, or even SAP Solution Manager, [Focused Run for SAP Solution Manager](https://support.sap.com/en/alm/focused-solutions/focused-run.html), or and [SAP Cloud ALM](https://support.sap.com/en/alm/sap-cloud-alm.html). For more information, see [SAP Alert Notification Service](https://help.sap.com/viewer/p/ALERT_NOTIFICATION).

 <a name="loiob21821e37ea14f69af731bf5811af338"/>

<!-- loiob21821e37ea14f69af731bf5811af338 -->

## Going Live

Once you've tested your application successfully and ensured that you are compliant with any applicable security guidelines and compliance regulations, you can go live with your application.

If you've set up a staged development environment, we recommend that your Cloud Administration Team defines specific timeframes during which the Cloud Development Team is allowed to go live with an application. You can forbid go-live activities during times that a stable landscape is particularly crucial \(for example, at the end of each quarter\), and allow deployments to your production subaccount only in case of emergencies.

Consider embedding applications with internal end users in the SAP Fiori launchpad using SAP BTP Portal before you go live. This enables your internal target audience to access all applications in one central place and thus improves the app's usability. For more information, see [SAP Cloud Portal Service](https://https://help.sap.com/viewer/ad4b9f0b14b0458cad9bd27bf435637d/Cloud/en-US/5798687972fd4c2bace31c65b47f5587.html).



<a name="loiob21821e37ea14f69af731bf5811af338__section_b2p_p5d_fpb"/>

## Manage Authentication and Authorization

Ensure that the business users of your application are being provided by using SAP ID service or configuring the trust relationship to an external identity provider. They should also get the right authorization by using application-based authorization artifacts provided by the developers. This allows the administrators to create roles, build role collections, and assign these collections to business users and user groups.

For more information, see [Security Administration: Managing Authentication and Authorization](https://help.sap.com/viewer/ae8e8427ecdf407790d96dad93b5f723/Cloud/en-US/1ff47b2d980e43a6b2ce294352333708.html "This section describes the tasks of administrators in the Cloud Foundry environment of SAP BTP. Administrators ensure user authentication and assign authorization information to users and user groups.") :arrow_upper_right: .



<a name="loiob21821e37ea14f69af731bf5811af338__section_lcm_pll_zgb"/>

## Web Acceleration

If your application's end users are widely spread across different countries or even continents, you can improve your application's load performance by using a Content Delivery Network \(CDN\). For example, you can use common CDN providers such as Akami or Cloudflare.

If you include SAP’s SAPUI5 library directly from *\*.hana.ondemand.com*, the SAPUI5 resources are automatically delivered via a CDN. See [Variant for Bootstrapping from Content Delivery Network](https://sapui5.hana.ondemand.com/#/topic/2d3eb2f322ea4a82983c1c62a33ec4ae).

Consider the following when using a CDN:

-   Secure transport: Make sure any access via HTTP will get redirected to a HTTPS connection before loading any content.

-   Block access based on location: If blocking access from a certain country is required, the client’s location data can be used. Keep in mind that this does not guarantee a full blocking, since the client’s location data can be changed, or the client could access from another country via a virtual private network \(VPN\).

-   Content compression: You can compress your content with gzip before it gets delivered to the client. This improves the performance, especially for clients with a slow connection.

-   Content caching: In addition to client caching, you can make the CDN provider cache your server’s content, so that following requests of the same resources by other clients will be delivered faster. While this can additionally improve the performance, you need to keep in mind the following:

    -   Make sure that you only cache static content. We recommend that you exclude certain files \(for example, for UI5 apps, exclude the neo-app.json file\) or paths \(for example, a route to OData services\), to make sure dynamic content is never cached.

    -   You should configure your CDN provider so that it respects the `Cache-Control` and `Expires` header of your server.

    -   You should not cache any dynamic header, such as the `X-CSRF-Token` header, that is used against cross-site request forgery \(CSRF\).


-   See [SAP Note 2943781](https://launchpad.support.sap.com/#/notes/SAP Note 2943781) for information about using CDN for on-premise systems.


