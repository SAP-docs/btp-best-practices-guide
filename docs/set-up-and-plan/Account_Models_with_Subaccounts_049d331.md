<!-- loio049d331effa3434c8b55995f63f92f5f -->

# Account Models with Subaccounts

Account Models 1 - 5 show ways to structure your global account into subaccounts. Note that all of them are just examples. They are not mutually exclusive and you can adapt them to your own needs.

Once your global account is migrated to cloud management tools, feature set B, you will be able to make use of one more hierarchical level within your global account: While account models 1 - 5 are still possible, with feature set B, you can additionally use directories and custom properties to group subaccounts. For more information, see [caf4e4e23aef4666ad8f125af393dfb2.md](caf4e4e23aef4666ad8f125af393dfb2.md) and [Account Models With Directories and Subaccounts \[Feature Set B\]](Account_Models_With_Directories_and_Subaccounts_Feature_Set_B_b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd).

-   **[Account Model 1: Create a Staged Development Environment Combining the Cloud Foundry and the Neo Environment](Account_Model_1_Create_a_Staged_Development_Environment_Combining_the_Cloud_Foundry_and_the_Neo_Environment_d109515.md)**  
In this scenario, the IT department of an organization creates a staged development environment by creating three subaccounts in both the Cloud Foundry and the Neo environment, in order to use SAP Web IDE Full-Stack, which only runs in the Neo environment.
-   **[Account Model 2: Use a Subaccount as a Base Template for Development Projects in the Neo Environment](Account_Model_2_Use_a_Subaccount_as_a_Base_Template_for_Development_Projects_in_the_Neo_Environment_f295f02.md)**  
In this scenario, the IT department creates one subaccount that serves as a base template. If new subaccounts for a development project are required, the IT department clones the base template, thereby copying its configuration settings to the new subaccounts.
-   **[Account Model 3: Use Separate Subaccounts for Data and API Management](Account_Model_3_Use_Separate_Subaccounts_for_Data_and_API_Management_c973258.md)**  
In this scenario, the IT department of an organization manages separate subaccounts for data isolation and for reuse of API management and connectivity. The department also creates dedicated \(staged\) subaccounts for development projects.
-   **[Account Model 4: Create a Staged Development Environment Using Continuous Integration / Continuous Delivery](Account_Model_4_Create_a_Staged_Development_Environment_Using_Continuous_Integration__Continuous_Delivery_c7788e6.md)**  
In this account model, a dedicated Development subaccount is created for each development project. Applications that are developed in these subaccounts are consolidated, tested, and published in one single Testing and Production subaccount.
-   **[Account Model 5: Create a Staged Development Environment Per Functional Area](Account_Model_5_Create_a_Staged_Development_Environment_Per_Functional_Area_8f57535.md)**  
In this scenario, the IT department creates separate Dev, Test, and Prod subaccounts for each functional area: In our example, HR, IT, and Sales each get their own subaccounts for development, test, and production.
-   **[When to Use Which Account Model](When_to_Use_Which_Account_Model_e4b4b5f.md)**  
Determine which account model with subaccounts is the most appropriate for your needs.

**Related Information**  


[Account Models With Directories and Subaccounts \[Feature Set B\]](Account_Models_With_Directories_and_Subaccounts_Feature_Set_B_b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd)

