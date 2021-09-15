<!-- loioa03d08e4038b46d480c410395593bbd2 -->

# Giving Access Rights to Platform Users

If you've set up a staged development environment using different subaccounts or spaces, such as for development, testing, and production, we recommend that you grant the Cloud Development Team access to development subaccounts and spaces, but that you grant only the Cloud Administration Team access to the testing and production subaccounts or spaces.

All developers and stakeholders for a particular development project or application should get access to the Development subaccount or space, if the project or application has been properly enrolled. See [Add Security Administrators to Your Subaccount [Feature Set A]](https://help.sap.com/viewer/50fd4b19521f4bec9ee9cc6c72a90872//en-US/fea877c449ba4c5fbb0aafd92a80afb4.html "Running on the cloud management tools feature set A: Security administrators manage the user and role assignments in their subaccounts. They also determine which identity providers their subaccounts trust.") :arrow_upper_right: and [Add Members to Your Subaccount [Feature Set B]](https://help.sap.com/viewer/50fd4b19521f4bec9ee9cc6c72a90872//en-US/1e1b7b60bb1b4764a2d4bb96bd73182d.html "Add members to your subaccount by assigning them a predefined role collection.") :arrow_upper_right:. We recommend that you assign all developers the **Space Developer** role, to enable them to develop, assign roles, and test the application's functionalities. You can also configure custom platform roles. See [Manage Custom Platform Roles](https://help.sap.com/viewer/663f91a6573b49ae9fa5f0007abb4d18/Internal/en-US/ede5f721e78e4d678c87c8a200c564ca.html "Subaccount administrators can define custom platform roles and assign them to the members of its subaccounts.") :arrow_upper_right:.

As every small change that's made in a single application \(for example, changing a destination\) might affect all other applications, only the Cloud Administration Team should have access to the test and prod subaccounts or spaces, and should manage them centrally. If required, developers may be assigned to the **User and Role Auditor** role to get read access. For all changes required in subaccounts or spaces, the Cloud Development Team should reach out to the Cloud Administration Team.

> ### Note:  
> To avoid overwhelming the Cloud Administration Team with inquiries, consider automating of tasks and providing a build infrastructure for continuous deployment.

**Related Information**  


[User and Member Management](https://help.sap.com/viewer/50fd4b19521f4bec9ee9cc6c72a90872//en-US/cc1c676b43904066abb2a4838cbd0c37.html "On the cloud platform, member management happens at all levels from global account to space, while user management is done for deployed applications.") :arrow_upper_right:

