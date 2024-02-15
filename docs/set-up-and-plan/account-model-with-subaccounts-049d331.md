<!-- loio049d331effa3434c8b55995f63f92f5f -->

# Account Model with Subaccounts

This simple account model shows how to structure your global account into three subaccounts, without making use of directories. It can later easily be expanded to make use of directories as further structuring elements.

In this scenario, the IT department creates separate Dev, Test, and Prod subaccounts for their development projects in different functional areas. In addition to the structuring according to functional areas, you can create separate dev, test, and prod subaccounts for large projects that use different components or services and have a completely separated support process and operations model than your other projects.

With a separate account landscape per functional area, you can use multiple instances of the same SaaS subscription \(e.g. in case you need to keep data or user access separated\). For example, HR subaccounts would use an internal identity provider, whereas for public or external scenarios, an external identity provider could be used.

Using this account model, you can distribute the subaccount administration to several teams, which allows for easy scaling as the number of cloud projects grows while still having a manageable amount of maintenance and governance efforts. If possible, consider assigning responsible colleagues to each group of three subaccounts, i.e. to each account landscape.

![](images/sap_cp_lm_account_model_scenarios_5_69892c5.png)

A SaaS application can only be used once within a subaccount, so if each functional area has their own subaccount \(for dev, test, and prod\), you won't encounter limitations as to using the same SaaS offering in different projects. Still, in the Cloud Foundry environment, you can separate different projects within a subaccount into different spaces.

In the Cloud Foundry environment, if you use a central Fiori Launchpad, and you want to deploy applications that use it in a different subaccount, use the [Launchpad Module](https://help.sap.com/viewer/ad4b9f0b14b0458cad9bd27bf435637d/Cloud/en-US/4dec640b19da4245be64383be24be173.html). If you want to create applications in the same subaccount as the Fiori launchpad, we recommend to deploy them to the HTML5 repository as described in [Developing HTML5 Applications](https://help.sap.com/viewer/ad4b9f0b14b0458cad9bd27bf435637d/Cloud/en-US/c1b9d6facfc942e3bca664ae06387e9b.html).

> ### Tip:  
> We recommend adding directories to structure your subaccounts, as soon as you have more than three subaccounts: [Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd).

**Related Information**  


[Account Model With Directories and Subaccounts](account-model-with-directories-and-subaccounts-b5a6b58.md#loiob5a6b58694784d0c9f4ff85f9b7336dd "The account models in this section show use cases for directories as structuring elements for your subaccounts.")

