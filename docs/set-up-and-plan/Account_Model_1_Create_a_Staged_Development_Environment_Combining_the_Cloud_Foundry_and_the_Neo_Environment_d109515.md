<!-- loiod109515c5f364cf4be167690f93ec079 -->

# Account Model 1: Create a Staged Development Environment Combining the Cloud Foundry and the Neo Environment

In this scenario, the IT department of an organization creates a staged development environment by creating three subaccounts in both the Cloud Foundry and the Neo environment, in order to use SAP Web IDE Full-Stack, which only runs in the Neo environment.

> ### Tip:  
> Check out SAP Business Application Studio, which is a modern development environment that runs in the Cloud Foundry environment, and which makes using the SAP Web IDE Full-Stack in the Neo environment unnecessary: [SAP Business Application Studio](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/8f46c6e6f86641cc900871c903761fd4.html).

Dedicated spaces for specific applications or projects are created in each of the subaccounts in the Cloud Foundry environment.

 ![](images/sap_cp_lm_account_model_scenarios_4_74c7980.png) 

If you need to deploy an application to a space within the Cloud Foundry environment, you can use SAP Web IDE Full-Stack, which runs in a subaccount in the Neo environment. In this case, we recommend that you create three subaccounts in the Cloud Foundry environment to separate the three different development stages. In addition, create one subaccount in the Neo environment that you use for developing using the SAP Web IDE Full-Stack. You can connect that subaccount with your Development and Testing subaccounts in the Cloud Foundry environment by configuring trust and destinations.

> ### Note:  
> This setup works only if you use the same identity provider for the subaccounts in the Cloud Foundry and in the Neo environments. For more information, see [Principal Propagation from Cloud Foundry to Neo](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f70fcf1c2d0a4a979adfe44cebc93c20.html)

**Related Information**  


<?sap-ot O2O class="- topic/link " href="f70fcf1c2d0a4a979adfe44cebc93c20.xml" text="" desc="" xtrc="link:1" xtrf="file:/c:/dita/edd1633942192239/src/cms/content/localization/en-US/d109515c5f364cf4be167690f93ec079.xml" ?>

[Configure Trust](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/f96e4c5930a94d1ba117e05a3f3c30fc.html)

[Configure Destinations from the Cockpit](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/60735ad11d8a488c83537cdcfb257135.html)

[When to Use Which Account Model](When_to_Use_Which_Account_Model_e4b4b5f.md "Determine which account model with subaccounts is the most appropriate for your needs.")

