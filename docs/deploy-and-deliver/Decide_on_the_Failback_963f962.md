<!-- loio963f9622c81b4161b9c34cc42069f320 -->

# Decide on the Failback

In the setup of your failover scenario, define whether a failback is needed and how it is performed.

Depending on the setup of your failover scenario, a failback is either optional or mandatory:

-   If you use an **active/active setup**, your applications in both data centers must be identical and provide the exact same functionality. In this setup, both data centers are of equal value. Therefore, a failback to the primary data center is not needed but performed automatically the next time a failover is triggered.

-   If you use an **active/passive setup** and your applications in both data centers slightly differ from each other, a failback to the primary data center is mandatory to provide the full functionality of your application.


> ### Recommendation:  
> In a basic scenario, you can hand over the failback to the users of your application, who perform the failback automatically when later trying to access the primary version of your application again. In this scenario, visually differentiate between your primary and secondary application so that they are constantly reminded to switch back to the primary one once they have completed their transaction. Unlike an automatic failback as soon as the primary data center is available again, this approach ensures that your users are not interrupted while completing a transaction. Instead, they can decide on their own when to switch back to the primary application.

**Parent topicColonSymbol** [Implementing Failover](Implementing_Failover_df972c5.md "")

**Previous topicColonSymbol** [Define How a Failover Is Detected](Define_How_a_Failover_Is_Detected_88b86db.md "Define in which cases the automatic failover from one data center to the other is triggered.")

