<!-- loio617af9b2610f4a85bab5f8107cfd33f2 -->

# Establishing a Provider/Subscriber Scenario Using Multitenancy

The provider/subscriber approach is one of the important scenarios that are supported with multitarget application.

SAP BTP allows you to develop and run multitenant \(tenant-aware\) applications. These applications, which must apply the multitarget application approach, run on a shared compute unit that can be used by multiple consumers \(tenants\). Each consumer accesses the application through a dedicated URL.

For example, SAP partners or central IT organizations can build and run multitenant apps in their provider accounts, deploy them using the multitarget application concept as providers, then deliver them as services to their customers or line of business subsidiaries in corresponding subscriber accounts via subscriptions.

One of the advantages of this approach is that the application lifecycle and resource management is centrally managed. A single deployment can serve several subscribing subaccounts, which eases onboarding of new customers and decreases the number of code versions to manage. This also eases the consumption, as the actual customers of the applications do not have to deploy solutions and manage corresponding resources.

For more information, see the following:

-   [Multitenancy Roles](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/48b552fa449945b9afc7885e1919ce2b.html "") :arrow_upper_right:

-   [Developing Multitenant Applications in the Neo Environment](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/54a76156cd114e5d928642b8dde47b91.html "In the Neo environment of SAP BTP, you can develop and run multitenant (tenant-aware) applications. These applications run on a shared compute unit that can be used by multiple consumers (tenants). Each consumer accesses the application through a dedicated URL.") :arrow_upper_right:

-   [Developing Multitenant Applications in the Cloud Foundry Environment](https://help.sap.com/viewer/6cdb9cff1d9b4877b9da90e5020a32d2//en-US/5e8a2b74e4f2442b8257c850ed912f48.html "In the Cloud Foundry environment, you can develop and run multitenant applications, and share them with multiple consumers simultaneously on SAP BTP.") :arrow_upper_right:


