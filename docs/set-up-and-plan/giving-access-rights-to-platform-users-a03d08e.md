<!-- loioa03d08e4038b46d480c410395593bbd2 -->

# Giving Access Rights to Platform Users

If you've set up a staged development environment using different subaccounts or spaces, such as for development, testing, and production, we recommend that you grant the Cloud Development Team access to development subaccounts and spaces, but that you grant only the Cloud Administration Team access to the testing and production subaccounts or spaces.

All developers and stakeholders for a particular development project or application should get access to the Development subaccount or space, if the project or application has been properly enrolled. See [Add Security Administrators to Your Subaccount [Feature Set A]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/fea877c449ba4c5fbb0aafd92a80afb4.html "Running on the cloud management tools feature set A: Security administrators manage the user and role assignments in their subaccounts. They also determine which identity providers their subaccounts trust.") :arrow_upper_right: and [Add Members to Your Subaccount [Feature Set B]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/1e1b7b60bb1b4764a2d4bb96bd73182d.html "Add members to your subaccount to enable users to access resources available there. Platform users manage subaccounts with cloud management tools, while business users consume subscribed applications and services.") :arrow_upper_right:. We recommend that you assign all developers the `Space Developer` role, to enable them to develop, assign roles, and test the application's functionalities. You can also configure custom platform roles. See [Manage Custom Platform Roles](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/ede5f721e78e4d678c87c8a200c564ca.html "Subaccount administrators can define custom platform roles and assign them to the members of its subaccounts.") :arrow_upper_right:.

> ### Caution:  
> The `Space Developer` role has broad rights within Cloud Foundry and, in particular, has access to the credentials used in various services and app bindings as well as other sensitive data. Users with this role can access the data in the environment, either directly through administration tools or indirectly through an application or other client.

In production environments, only give this role to members of the Cloud Administration Team that are authorized to access data in the environment.

In cases where even the Administration Team isn't allowed to see or access the data, automate tasks that require the `Space Developer` role or integrate them into a deployment pipeline using a technical user with the `Space Developer` role. Firefighter situations where temporary use of the role is required for manual actions by an actual administrative user can be handled by temporary assignment of the `Space Developer` role. You can also use a special user account with the role whose credentials are only given out when needed and changed immediately after use. Remember to log the use of this role in an audit trail or another tracking tool.

As every small change that's made in a single application \(for example, changing a destination\) might affect all other applications, only the Cloud Administration Team should have access to the test and prod subaccounts or spaces, and should manage them centrally. If required, developers may be assigned to the `User and Role Auditor` role to get read access. For all changes required in subaccounts or spaces, the Cloud Development Team should reach out to the Cloud Administration Team.

> ### Note:  
> To avoid overwhelming the Cloud Administration Team with inquiries, consider automating of tasks and providing a build infrastructure for continuous deployment.

**Related Information**  


[User and Member Management](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cc1c676b43904066abb2a4838cbd0c37.html "On the cloud platform, member management happens at all levels from global account to space, while user management is done for deployed applications.") :arrow_upper_right:

