<!-- loio61d08d8c85f448a0b7399e83f01a1a04 -->

# Deploy Your Application in Two Data Centers

Deploy your application in two data centers in parallel so that in case of an issue, you can switch from one to the other.

To implement failover in an active/passive setup, deploy your application in two data centers in parallel. Among these two data centers, define the primary \(active\) one to which the traffic is generally directed and the secondary \(passive\) data center that takes over in case of a downtime.

Depending on your type of global account on SAP BTP and the environment you're using, you can choose from different regions to deploy your applications. To deploy an application in subaccounts of multiple regions, execute the deployment separately for each subaccount. For more information about regions and a complete list of data centers from which you can choose, see [Regions](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/350356d1dc314d3199dca15bd2ab9b0e.html).

> ### Recommendation:  
> To optimize the performance of your application, which is, for example, response time and latency, we recommend that you deploy it in two data centers of the region your target audience and your back-end system are located in. If you are located in Europe, choose, for example, the data centers in Frankfurt and Amsterdam.

> ### Note:  
> If you want to deploy your application in two data centers that are not located in the same region, keep in mind that there might be issues concerning legal data processing restrictions. For more information, see [Data Protection and Privacy](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7e513d31704a4a87831191e504ca850a.html).

**Parent topicColonSymbol** [Implementing Failover](Implementing_Failover_df972c5.md "")

**Next topicColonSymbol** [Keep the Two Applications in Sync](Keep_the_Two_Applications_in_Sync_e6d2bdb.md#loioe6d2bdb006734bd69e394379ff0dd956 "Synchronize your applications in both data centers to maintain their functionality in case of a downtime.")

