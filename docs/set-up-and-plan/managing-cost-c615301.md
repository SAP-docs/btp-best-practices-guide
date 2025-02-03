<!-- loioc615301dc2a14e34bc6ee2216c3368b1 -->

# Managing Cost

Consumption-based commercial models offer flexibility to optimize your costs. To manage these costs and avoid charges for overage, it's recommended that you monitor your usage and consumption.



<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_choose_commercial_model"/>

## Choose the Right Commercial Model

There are several commercial models for consuming SAP BTP services. Choosing the right commercial model is important for managing and predicting cost:

-   For established use cases with a fixed set of services and a known quantity, use the **subscription-based** model.

-   For more flexibility, especially during pilot stages of projects and for dynamically changing requirements, use a **consumption-based** model.


For details, see [Commercial Models](../basic-platform-concepts/basic-platform-concepts-38ecf59.md#loio263d40009a5a4237a62e8f5c05ee641e).



<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_provision_contracts_into_globalaccounts"/>

## Manage Provisioning of Contracts Into Global Accounts

Because billing happens on global account level, you must know to which global account a new contract is being provisioned. There are several options:

-   Provisioning of multiple subscription-based contracts into the same global account:

    Consolidating all services provisioned on SAP BTP into a single global account can help reduce the total cost of ownership \(TCO\), prevent “silos” of SAP BTP usage across the organization, and enables optimized usage of the available licenses.

-   Provisioning of a new consumption-based contract into existing global account:

    In such a “hybrid account” scenario, any usage that isn't covered by the associated subscription-based contracts is charged with the consumption-based model \(pay-per-use\). To avoid unintended overage billing, make sure to review the current usage and active subscription contracts.

-   Provisioning of multiple consumption-based contracts into separate global accounts:

    Multiple consumption-based contracts cannot be provisioned into the same global account. If you need fully separate bills \(for example, for different business entities\), having different global accounts can be an option. However, available credits cannot be transferred between global accounts.




<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_allocate_resources"/>

## Manage Resource Allocation and Avoid Over-Provisioning

To control consumption of services, set up a strict account model with the respective administrative authorizations. For details, see [Setting Up Your Account Model](setting-up-your-account-model-2db81f4.md).

Only provide the minimal required set of entitlements and quota to subaccounts.

Be aware that for services with unlimited quota, usage can potentially increase beyond the planned or budgeted volume. Therefore, consider additional measures, such as establishing a governance process for assigning application roles to users.



<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_monitor_usage_and_cost"/>

## Monitor Usage and Cost

In SAP BTP cockpit, go to *Costs and Usage* to monitor current and past usage of services, both on a global account level, and directory or subaccount level. It's recommended to do this at least once a month.

For example, you can use the reports to check how much individual services contribute to the total cost, and how cost or usage have evolved over time. Filter by directories and subaccounts, or use labels to filter based on custom criteria. For details, see [Labels](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/8ed4a705efa0431b910056c0acdbf377.html#loioe8663c08ead648faa673b0d63c5b478e "Labels are user-defined words or phrases that you can assign to various entities in SAP BTP to categorize them in your global account, to identify them more easily.") :arrow_upper_right:.

For accounts with a consumption-based commercial model, check your current cloud credit balance and if necessary, take mitigation actions to avoid overconsumption.

For hybrid accounts \(accounts with both consumption- and subscription-based contracts\), check the prepaid quota from the subscription and what is charged under the consumption-based model.



<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_validate_monthly_bills"/>

## Validate Monthly Bills

If you have a consumption-based contract, go to *Billing* in SAP BTP cockpit to validate the information in your monthly balance statements.

The current month is shown as an estimation, until the billing of the current month has closed. The balance statement is ordered according to the product column. You can also analyze the balance statements further, for example, by drilling into the cost for a subaccount and individual service.

> ### Tip:  
> Instead of manually checking usage and costs, you can also set up automatic alerts using the SAP Usage Data Management service in combination with the SAP Alert Notification service for SAP BTP. For an example, see [BTP Resource Consumption Monitor](https://github.com/SAP-samples/btp-resource-consumption-monitor).



<a name="loioc615301dc2a14e34bc6ee2216c3368b1__section_distribute_costs"/>

## Distribute Costs Across Internal Consumers

If you want to cross-charge cost to internal consumers, you can use the data in SAP BTP cockpit, *Costs and Usage*, to split cost by directory or subaccount.

You can also use labels, for example, to assign individual subaccounts or directories to a cost center or project, and then report on the cost by label.

Alternatively, you can export the data to a spreadsheet, or use the Public API of the SAP Usage Data Management service for further processing.

For services that are shared between multiple subaccounts, you can either use a fixed rate \(for example, per employee or per user\) or try to report the exact usage per consumer with a service-specific metric \(like the number of API calls, page views, or used storage\).

