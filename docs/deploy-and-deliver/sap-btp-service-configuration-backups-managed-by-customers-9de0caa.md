<!-- loio9de0caa8abe34f4897e5b727868019c0 -->

# SAP BTP Service Configuration Backups Managed by Customers

This document aims to clarify the backup strategy for SAP Business Technology Platform \(SAP BTP\) services, specifically focusing on service configurations managed by you, the customer. It isn't intended to serve as a comprehensive guide for all high availability and disaster recovery topics. For more information on resilience, high availability, and disaster recovery, see [Resilience, High Availability, and Disaster Recovery](https://help.sap.com/docs/btp/sap-business-technology-platform/resilience-high-availability-and-disaster-recovery?version=Cloud).



<a name="loio9de0caa8abe34f4897e5b727868019c0__section_jlw_b2w_1dc"/>

## Prerequisites

You must be aware which SAP BTP services you're currently using:

-   If you already have a global account on SAP BTP, contact the Global Account Administrator of the global account for a list of the services that you're currently using. If you’re unsure who this person is, contact your SAP Sales representative.

-   If you don't have a global account yet, see [Getting a Global Account](https://help.sap.com/docs/btp/sap-business-technology-platform/getting-global-account?version=Cloud).




<a name="loio9de0caa8abe34f4897e5b727868019c0__section_u5q_mbm_r4b"/>

## How to Back Up Your Service Configurations

SAP doesn't manage backups of service configurations. You're responsible for backing up your service-specific configurations to ensure you can restore them if they're accidentally deleted. For services with user-specific backup capabilities, it's crucial to regularly back up configurations to prevent data loss and ensure continuity. You must familiarize yourself with the documentation of your specific services to effectively manage and restore configurations when needed.

> ### Note:  
> You must back up your service configurations yourself to ensure you have backups. Some services don't include user-specific configurations in [Data Backups Managed by SAP](https://help.sap.com/docs/btp/btp-admin-guide/data-backups-managed-by-sap?version=Cloud).



<a name="loio9de0caa8abe34f4897e5b727868019c0__section_j41_hhv_jcc"/>

## Where to Find Backup Information for User-Specific Configurations

Service configurations vary and can be backed up depending on the specific service you use. If a service allows for configuration backups, backup information is part of your service documentation. In case you're unable to find the information you need, refer to [Getting Support](https://help.sap.com/docs/btp/sap-business-technology-platform/btp-getting-support?version=Cloud) for an overview of available support channels and instructions about how to get assistance.



<a name="loio9de0caa8abe34f4897e5b727868019c0__section_h4l_4bm_r4b"/>

## Services Lacking Backup Options for User-Specific Configurations

Certain services don't support the backup of user-specific configurations either due to specifics of the services' functionality \(for example, a service that doesn't require any user configurations\) or due to this feature being still in development. Check you service's documentation to be aware of the limitations and to plan accordingly. If you need support, refer to [Getting Support](https://help.sap.com/docs/btp/sap-business-technology-platform/btp-getting-support?version=Cloud) for an overview of available support channels and instructions about how to get assistance.

**Related Information**  


[Data Backups Managed by SAP](data-backups-managed-by-sap-6c1e071.md "SAP handles the backup and recovery of service data. However, there are some exceptions.")

