<!-- loioc973258cbb9a4e399b0d5ec988ead034 -->

# Account Model 3: Use Separate Subaccounts for Data and API Management

In this scenario, the IT department of an organization manages separate subaccounts for data isolation and for reuse of API management and connectivity. The department also creates dedicated \(staged\) subaccounts for development projects.

Access to back-end systems is managed centrally by the IT department via API management in three dedicated subaccounts. Every new development project uses separate subaccounts \(one each for Development, Test, and Production\) that consumes the APIs that are managed in these subaccounts via destinations. In addition, SAP HANA databases are deployed in two dedicated subaccounts – Development/Testing and Production – and shared across different subaccounts.

The advantages of this model are that it allows you to scale quickly while ensuring that connections to your back-end systems are always established via APIs; it also keeps costs low \(due to the sharing of the SAP HANA databases across subaccounts\).

 ![](../images/sap_cp_lm_account_model_scenarios_2_029bbee.png) 

