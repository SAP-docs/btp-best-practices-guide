<!-- loio6c1e071845dd4db2829b413a05154a7c -->

# Data Backups Managed by SAP

SAP handles the backup and recovery of service data. However, there are some exceptions.



<a name="loio6c1e071845dd4db2829b413a05154a7c__section_wg4_p1m_r4b"/>

## Services with Automated Data Backups

Data stored in the following services and components is automatically backed up on a regular basis by SAP:

-   **SAP HANA Cloud**: SAP HANA Cloud instances are continually backed up to safeguard your database and ensure that it can be recovered. For more information, see [Backup and Recovery](https://help.sap.com/docs/HANA_CLOUD/9ae9104a46f74a6583ce5182e7fb20cb/89d71f01daca4ecaaa069d6a060167f5.html).

-   **PostgreSQL on SAP BTP, Hyperscaler Option**: SAP keeps backups of your PostgreSQL database instances for a retention period of 14 days. You can restore a database instance to any point in time within the backup retention period by creating a new database instance. For more information, see [Restore Database Instance to a Specified Time](https://help.sap.com/viewer/b3fe3621fa4a4ed28d7bbe3d6d88f036/Cloud/en-US/724c9112ed5a48c59c8e88f17290550d.html).




<a name="loio6c1e071845dd4db2829b413a05154a7c__section_dbc_r1m_r4b"/>

## Services Without Automated Data Backups

The following services don’t currently provide any backup and restore features:

-   **Redis on SAP BTP, hyperscaler option**: This service doesn’t support persistence.

-   **Object Store on SAP BTP**: There's no backup and restore feature provided by the Object Store service. However, there are additional features that could help with backup and restore in certain scenarios:

    -   [Object Versioning](https://help.sap.com/viewer/2ee77ef7ea4648f9ab2c54ee3aef0a29/Cloud/en-US/787fbe77f4eb46e0ae9a6222d57ba50e.html) allows you to recover from accidental deletion and modification of objects because the hyperscalers keep older versions in case the objects are modified or deleted.

    -   [Object Expiration Rules](https://help.sap.com/viewer/2ee77ef7ea4648f9ab2c54ee3aef0a29/Cloud/en-US/52e2c18af86c45e2b1495cd594602304.html) helps with the automatic deletion of older versions.

    -   The **prevent deletion** feature helps preventing your blob stores from accidental deletion. For more information, see [Prevent Accidental Deletion of AWS S3 Buckets](https://help.sap.com/viewer/2ee77ef7ea4648f9ab2c54ee3aef0a29/Cloud/en-US/8c3c66da50364e0bafb994f4c4b57042.html) and [Preventing Accidental Deletion of Azure Containers](https://help.sap.com/viewer/2ee77ef7ea4648f9ab2c54ee3aef0a29/Cloud/en-US/67e5ba7dae7749c88483b8a3fe395eff.html)





<a name="loio6c1e071845dd4db2829b413a05154a7c__section_vgj_qk3_mbc"/>

## Runtimes



### SAP BTP, Cloud Foundry Runtime

For services running in the SAP BTP, Cloud Foundry runtime, the backed-up data is copied to additional availability zones within the same region. Each availability zone represents a physically separate location with its own power supply, network, and cooling. For more information, see [Regions](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/350356d1dc314d3199dca15bd2ab9b0e.html).

![](images/Data_copied_to_additional_AZs_in_a_region_6198557.png)



### SAP BTP, Kyma Runtime

SAP BTP, Kyma runtime relies on managed Kubernetes clusters for periodic backups of Kubernetes objects. Automatic backup doesn't include Kubernetes volumes. For more information, see [Kyma Environment Backup](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/ab959cfbd07b46af97aecfd6577bfb10.html).



### SAP BTP, Neo Environment

For services running in the **SAP BTP, Neo** environment, the backed-up data is copied to an availability zone in another region. For more information, see [Regions in the Neo Environment](https://help.sap.com/viewer/ea72206b834e4ace9cd834feed6c0e09/Cloud/en-US/21c30a4e491544fc927ecf3a5857c54e.html).

![](images/Data_copied_to_a_secondary_AZ_449d088.png)



### SAP BTP ABAP Environment

The ABAP environment relies on backups from SAP HANA Cloud. For details, see [Backups](https://help.sap.com/docs/btp/sap-business-technology-platform/backups?state=DRAFT&version=Cloud).

**Related Information**  


[SAP BTP Service Configuration Backups Managed by Customers](sap-btp-service-configuration-backups-managed-by-customers-9de0caa.md "This document aims to clarify the backup strategy for SAP Business Technology Platform (SAP BTP) services, specifically focusing on service configurations managed by you, the customer. It isn't intended to serve as a comprehensive guide for all high availability and disaster recovery topics. For more information on resilience, high availability, and disaster recovery, see Resilience, High Availability, and Disaster Recovery.")

