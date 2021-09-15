<!-- loio1dbce9caa4314103bbc9a7e3ca548280 -->

# Setting Up Authentication

SAP BTP provides various options for implementing user authentication.

Use the decision tree below to determine how to set up authentication. Once you've implemented authentication, you can start implementing user authorization.

> ### Remember:  
> There are two types of users on SAP BTP: platform and business. Platform users are usually developers, administrators, or operators who deploy, administer, and troubleshoot applications and services. Business users are those who use the applications that are deployed to SAP BTP.

   
  
<a name="loio1dbce9caa4314103bbc9a7e3ca548280__fig_d4w_mrw_42b"/>Setting Up Authentication

 ![](../images/sap_cp_lm_authentication_49d26c9.png "Setting Up Authentication") 

Users can be authenticated by the Identity Authentication service or by the SAP ID Service \(default\).

> ### Recommendation:  
> We recommend that you use the Identity Authentication service and also connect any corporate IdPs to it.
> 
> > ### Note:  
> > For platform users of feature set B, IdP is not yet available.

The Identity Authentication service can authenticate users stored in the IAS user store, your own corporate user store, or by forwarding to your own corporate identity provider.

-   **[Authentication Methods](Authentication_Methods_9751f1b.md "You can implement the authentication methods that are available on SAP BTP on the frontend of
		applications. ")**  
You can implement the authentication methods that are available on SAP BTP on the frontend of applications.
-   **[Destination Authentication Methods](Destination_Authentication_Methods_765423d.md "Destinations are part of SAP BTP Connectivity and are
		used for communication between a cloud application and a remote system. ")**  
Destinations are part of SAP BTP Connectivity and are used for communication between a cloud application and a remote system.

**Related Information**  


[Set up Platform Identity Provider](https://help.sap.com/viewer/663f91a6573b49ae9fa5f0007abb4d18/Internal/en-US/80edbe70b8f3478d8a59c21a91a47aa6.html "The platform identity provider is the user base for access to your SAP BTP subaccount in the Neo environment. The default user base is provided by SAP ID Service. You can switch to an Identity Authentication tenant if you want to use a custom user base.") :arrow_upper_right:



[Trust and Federation with Identity Providers](https://help.sap.com/viewer/50fd4b19521f4bec9ee9cc6c72a90872//en-US/cb1bc8f1bd5c482e891063960d7acd78.html "When setting up accounts you need to assign users. While we provide you with your first users to get you started, your organization has its own user bases which you want to integrate.") :arrow_upper_right:

[Identity Authentication](https://www.sap.com/community/topics/cloud-platform-identity-authentication.html)

