<!-- loioa03d08e4038b46d480c410395593bbd2 -->

# Giving Access Rights to Platform Users

If you've set up a staged development environment using different subaccounts or spaces, such as for development, testing, and production, grant the Cloud Development Team access to development subaccounts and environments. Only grant the Platform Engineering Team or Center of Expertise \(CoE\) access to the testing and production subaccounts or environments.

All developers and stakeholders for a particular development project or application should get access to the development subaccount or environment, if the project or application has been properly enrolled. We recommend that you assign all developers authorizations to develop, assign roles, and test the application's functionalities.

In cases where even the Platform Engineering Team/CoE isn't allowed to see or access the data, automate tasks that require developer access or integrate them into a deployment pipeline using a technical user with the developer authorizations. Firefighter situations where temporary use of the role is needed for manual actions by an actual administrative user can be handled by temporary assignment of the developer access. You can also use a special user account with access whose credentials are only given out when needed and changed immediately after use. Remember to log the use of this role in an audit trail or another tracking tool.

As every small change that's made in a single application \(for example, changing a destination\) can affect all other applications. Only grant the Platform Engineering Team/CoE access to the test and prod subaccounts or environments. Have this team manage them centrally. If necessary, assign developers read access. For all changes required in subaccounts or spaces, the Cloud Development Team should reach out to the Platform Engineering Team/CoE.

  
  
**Division of Access to Different Stages of the Development Pipeline**

![](images/dev_pipeline_best_practices_pptx_6451607.png "Division of Access to Different Stages of the Development Pipeline")

> ### Tip:  
> To avoid overwhelming the Platform Engineering Team/CoE with inquiries, consider automating tasks and providing a build infrastructure for continuous deployment.



<a name="loioa03d08e4038b46d480c410395593bbd2__section_oz4_t5p_dyb"/>

## Global Accounts and Directories

Platform users depend on role collections for access at the global account and directory level. By default, user management isn't enabled for directories. To manage platform users at this level, use SAP BTP cockpit or the btp cli.

For more information, see:

-   [Add Members to Your Global Account](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/4a0491330a164f5a873fa630c7f45f06.html "Add users as global account members using the SAP BTP cockpit.") :arrow_upper_right:

-   [Manage Users in Directories](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/ff4d4a4caff94b0486b6427eaa8a0b91.html "Manage members in your directory using the SAP BTP cockpit.") :arrow_upper_right:

-   [Role Collections and Roles in Global Accounts, Directories, and Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/0039cf082d3d43eba9200fe15647922a.html "SAP BTP provides a set of role collections to set up administrator access to your global account and subaccounts.") :arrow_upper_right:




<a name="loioa03d08e4038b46d480c410395593bbd2__section_pc4_dbx_byb"/>

## Multi-Environment Subaccounts

See [Add Members to Your Subaccount](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1e1b7b60bb1b4764a2d4bb96bd73182d.html "Add members to your subaccount to enable users to access resources available there. Platform users manage subaccounts with cloud management tools, while business users consume applications and services.") :arrow_upper_right:.



### Cloud Foundry

We recommend that you assign all developers the `Space Developer` role, so they can develop, assign roles, and test the application's functionalities.

> ### Caution:  
> The `Space Developer` role has broad rights within Cloud Foundry and, in particular, has access to the credentials used in various services and app bindings as well as other sensitive data. Users with this role can access the data in the environment, either directly through administration tools or indirectly through an application or other client.

In production environments, only give this role to members of the Platform Engineering Team/CoE that are authorized to access data in the environment.

For more information, see [About User Management in the Cloud Foundry Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/8e6ce969c432437dbaecedea385df8c8.html).



### ABAP

Platform users in the ABAP environment depend on Cloud Foundry. Administrators need the `Org Manager` and `Space Manager` roles. Developers need the `Space Developer` role. The same recommendations apply as in the Cloud Foundry environment to members of the Cloud Development and Platform Engineering/CoE teams.

In addition, platform users need the relevant business roles of the ABAP system: `SAP_BR_ADMINISTRATOR` and `SAP_BR_DEVELOPER`.

For more information, see [Creation of Additional Administrator Users](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ced83807a6dc4e33a2cfcdce06e9f9f3.html) and [Creation of Developer Users](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/f87151e385ba428cb7d12d0085060ebc.html).



### Kyma

You can assign roles to a group of users only if you use a custom identity provider. Assigning roles in Kyma is based on the Kubernetes [role-based access control](https://kubernetes.io/docs/reference/access-authn-authz/rbac/) \(RBAC\). Once you become the admin, your user name is read from the SAP BTP \(RBAC\) concept and is passed to the Kyma provisioner to be bound to the `cluster-admin` role in Kyma.

Because the development of a role concept is very specific for each organization, it’s recommended that you start with a very simple role concept: As a starting point, just separate the developers and operators of a cluster. Later, you can refine the role concept as needed.

For more information, see [Role-Based Access Control \(RBAC\) in Kyma](role-based-access-control-rbac-in-kyma-bb31080.md) and [Assign Roles in the Kyma Environment](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/148ae38b7d6f4e61bbb696bbfb3996b2.html).



<a name="loioa03d08e4038b46d480c410395593bbd2__section_kc1_fbx_byb"/>

## Neo Subaccounts

Assign the predefined platform roles for platform users. You can also configure custom roles.

For more information, see:

-   [Managing Member Authorizations in the Neo Environment](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/a1ab5c4cc117455392cd0a512c7f890d.html "SAP BTP includes predefined platform roles that support the typical tasks performed by users when interacting with the platform. In addition, subaccount administrators can combine various scopes into a custom platform role that addresses their individual requirements.") :arrow_upper_right:

-   [Manage Custom Platform Roles](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/ede5f721e78e4d678c87c8a200c564ca.html "Subaccount administrators can define custom platform roles and assign them to the members of its subaccounts.") :arrow_upper_right:


**Related Information**  


[User and Member Management](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cc1c676b43904066abb2a4838cbd0c37.html "On SAP BTP, user management takes place at all levels from global account to environment. There are different types of users, such as depending on their roles in the company.") :arrow_upper_right:

