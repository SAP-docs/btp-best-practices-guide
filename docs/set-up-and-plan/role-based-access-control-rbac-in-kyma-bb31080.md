<!-- loiobb31080fd0474d38a050e32a7a7ed629 -->

# Role-Based Access Control \(RBAC\) in Kyma

Assigning permissions in Kyma is based on the Kubernetes role-based access control \(RBAC\). It’s recommended that you start with separating the developers and operators of a cluster. Later, you can refine the role concept as required.



<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_role_setup"/>

## Recommended Role Setup

The goal of the recommended role setup is to implement Kubernetes RBAC best practices, which is a method of regulating access to computer or network resources based on the roles of individual users within your organization.

The role setup separates the operators from the development teams, and day-to-day user accounts from administrative accounts. It enables DevOps while ensuring security on production clusters.

In production clusters and development and test clusters alike, each service, project, or development team should have its own namespace.

Typically, it‘s useful that developers have read access to dedicated resources on cluster level or in other namespaces, such as “Istio” or “Application Connector”. Use the ClusterRole `common-resource-viewer` for this. Additional modules can bring additional resources. For more information, see [Kyma Modules](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/0dda141a58d54f29a860a4b3164bf4a9.html "With Kyma's modular approach, you can install just the modules you need, instead of a predefined set of components.") :arrow_upper_right:.

-   The suggested setup uses the [Kubernetes objects](https://kubernetes.io/docs/reference/access-authn-authz/rbac/#api-overview) “ClusterRole”, “RoleBinding”, and “ClusterRoleBinding”. For examples of the required Kubernetes objects, see the suggested manifest templates.

-   In RoleBindings and ClusterRolebindings, use groups instead of users. For more information about group management in SAP Cloud Identity Services, see [Groups](https://help.sap.com/docs/IDENTITY_AUTHENTICATION/aa08922a434a456ba44982c9f4f4d790/ddd067c899f94e2f9006cc4dd417be80.html?locale=en-US).

-   To reduce the number of accounts directly assigned to powerful roles in the cluster, use Kubernetes impersonation.




### Impersonation in Kubernetes

With Kubernetes [User Impersonation](https://kubernetes.io/docs/reference/access-authn-authz/authentication/#user-impersonation), you can enable a least-privilege type of access to the Kubernetes cluster. With this feature, a subject \(that is, users, groups, or service accounts\) can acquire another Kubernetes user or group identity. These acquired identities are called “virtual users” or “vUser” because they don't need to exist.

Just create a ClusterRoleBinding that contains a virtual user \(`vUserName`\) and the administrative ClusterRole. For example, the operator or developer is allowed to impersonate the virtual user to perform administrative tasks.

![](images/Kubernetes_Impersonation_f6426e5.svg)



<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_operators_all_clusters"/>

## Role Setup for Operators

By default, operators only have view access in the clusters.

By impersonating a virtual user \(`cluster-admin`\) bound to the ClusterRole `cluster-admin`, the operator can perform administrative tasks.

![](images/Role_Concept_Operator_All_392ef0f.svg)



<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_devtest_cluster_roles"/>

## Role Setup for Developers \(Dev and Test\)

In **Dev** and **Test** clusters, developers have full access to their namespaces. In the namespace, bind them to the ClusterRole `admin`.

![](images/Role_Concept_Developer_DevTest_4e24b33.svg)



<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_prod_cluster_roles"/>

## Role Setup for Developers \(Prod\)

In **Prod** clusters, developers only have view access to their namespace. In the namespace, bind them to the ClusterRole `cluster-viewer`.

By impersonating a virtual user \(`<app-admin>`\) bound to the ClusterRole `admin`, a developer can perform administrative tasks in their namespace.

![](images/Role_Concept_Developer_PROD_8dccb86.svg)



> ### Tip:  
> Use the following manifest templates to set up the recommended role concept.
> 
> Expand the sections to see the role setup for each purpose, and within the sections, expand the sample code to see the manifest templates.



<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_kubernetes_manifest_templates_generic"/>

## Kubernetes Manifest Templates for Generic Roles



### View All Resources

Used in **Dev**, **Test**, and **Prod** clusters:

-   ClusterRole `cluster-viewer`

    > ### Sample Code:  
    > ```
    > # ClusterRole with the permission to view all resources
    > kind: ClusterRole
    > apiVersion: rbac.authorization.k8s.io/v1
    > metadata:
    >   name: cluster-viewer
    > rules:
    >   - apiGroups: ['*']
    >     verbs: ['get', 'list', 'watch']
    >     resources: ['*']
    > ```




### View Common Kyma Objects in the Cluster

Used in **Dev**, **Test**, and **Prod** clusters:

-   ClusterRole `common-resource-viewer`

    > ### Sample Code:  
    > ```
    > # ClusterRole with the permissions to view common Kyma objects in the cluster
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRole
    > metadata:
    >   name: <common-resource-viewer>
    > rules:
    >   - verbs:
    >       - get
    >       - list
    >       - watch
    >     apiGroups:
    >       - applicationconnector.kyma-project.io
    >       - networking.istio.io
    >     resources:
    >       - applications
    >       - gateways
    >     resourceNames: []
    >     nonResourceURLs: []
    > ```

-   ClusterRoleBinding `common-resource-viewer-crb`

    > ### Sample Code:  
    > ```
    > # ClusterRoleBinding to allow a group to view common Kyma objects in the cluster
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRoleBinding
    > metadata:
    >   name: <common-resource-viewer-crb>
    > subjects:
    >   - kind: Group
    >     name: <group-name>
    >     apiGroup: rbac.authorization.k8s.io
    > roleRef:
    >   kind: ClusterRole
    >   name: common-resource-viewer
    >   apiGroup: rbac.authorization.k8s.io
    > 
    > ```




<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_kubernetes_manifest_templates_operators"/>

## Kubernetes Manifest Templates for Operators



### View Access for All Clusters

Used in **Dev**, **Test**, and **Prod** clusters:

-   ClusterRoleBinding `cluster-admin-view-crb`

    > ### Sample Code:  
    > ```
    > # Default permissions for the ops-team group to view all resources in the cluster
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRoleBinding
    > metadata:
    >   name: cluster-admin-view-crb
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: cluster-viewer
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: Group
    >     name: <group-name>
    > 
    > ```




### Admin Access for All Clusters

Used in **Dev**, **Test**, and **Prod** clusters:

-   ClusterRoleBinding `cluster-admin-crb`

    > ### Note:  
    > The ClusterRole `cluster-admin` is not directly bound to the group of the operations team, they can only impersonate it.

    > ### Sample Code:  
    > ```
    > # ClusterRoleBinding to allow the (not really existing) user cluster-admin to have cluster-admin permissions on the cluster. The ClusterRole cluster-admin is NOT directly bound to the ops-team group.
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRoleBinding
    > metadata:
    >   name: cluster-admin-crb
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: cluster-admin
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: User
    >     name: cluster-admin
    > 
    > ```

-   ClusterRole `cluster-admin-impersonator`

    > ### Sample Code:  
    > ```
    > # ClusterRole to allow the impersonation of the cluster-admin user
    > 
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRole
    > metadata:
    >   name: cluster-admin-impersonator
    > rules:
    >   - apiGroups: ['']
    >     resources: ['users']
    >     verbs: ['impersonate']
    >     resourceNames: ['cluster-admin']
    > 
    > ```

-   ClusterRoleBinding `cluster-admin-impersonate-crb`

    > ### Sample Code:  
    > ```
    > # ClusterRoleBinding to bind the impersonation capability to everyone in the ops-team group
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRoleBinding
    > metadata:
    >   name: cluster-admin-impersonate-crb
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: cluster-admin-impersonator
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: Group
    >     name: <group-name>
    > ```




<a name="loiobb31080fd0474d38a050e32a7a7ed629__section_kyma_kubernetes_manifest_templates_developers"/>

## Kubernetes Manifest Templates for Developers



### Namespace Admin Access for Dev and Test

Used in **Dev** and**Test** clusters:

-   RoleBinding `admin`

    > ### Sample Code:  
    > ```
    > 
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: RoleBinding
    > metadata:
    >   name: <name>
    >   namespace: <name of the namespace>
    > subjects:
    >   - kind: Group
    >     name: <group name>
    >     apiGroup: rbac.authorization.k8s.io
    > roleRef:
    >   kind: ClusterRole
    >   name: admin
    >   apiGroup: rbac.authorization.k8s.io
    > 
    > ```




### Admin Access for Prod

Create the respective manifest files for each team and namespace, and adapt them accordingly.

Used in **Prod** clusters:

-   ClusterRole `app-admin-impersonator`

    > ### Sample Code:  
    > ```
    > # ClusterRole to allow the impersonation of the application admin user
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRole
    > metadata:
    >   name: <app-admin-impersonator>
    > rules:
    >   - apiGroups: ['']
    >     resources: ['users']
    >     verbs: ['impersonate']
    >     resourceNames: ['<name of the virtual user>']
    > 
    > ```

-   ClusterRoleBinding `app-team-impersonation-crb`

    > ### Sample Code:  
    > ```
    > # ClusterRoleBinding to bind the impersonation capability to the app-team group
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: ClusterRoleBinding
    > metadata:
    >   name: <app-team-impersonation-crb>
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: <app-admin-impersonator>
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: Group
    >     name: <group-name>
    > 
    > ```

-   RoleBinding `admin`

    > ### Note:  
    > The ClusterRole `admin` is not directly bound to the groups of the development teams, they can only impersonate it.

    > ### Sample Code:  
    > ```
    > # RoleBinding to allow a (not really existing) user to have admin permissions in a specific namespace. The ClusterRole admin is NOT directly bound to the developers groups.
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: RoleBinding
    > metadata:
    >   name: <binding name, e.g. app1-admin-crb>
    >   namespace: <namespace>
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: admin
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: User
    >     name: <name of the virtual user>
    > 
    > ```




### Read Access to Namespace for Prod

Create the respective manifest files for each team and namespace, and adapt them accordingly.

Used in **Prod** clusters:

-   RoleBinding `cluster-viewer`

    > ### Sample Code:  
    > ```
    > # Default permissions of an app-team group to view all resources in a dedicated namespace
    > apiVersion: rbac.authorization.k8s.io/v1
    > kind: RoleBinding
    > metadata:
    >   name: <namespace-viewer-binding>
    >   namespace: <namespace>
    > roleRef:
    >   apiGroup: rbac.authorization.k8s.io
    >   kind: ClusterRole
    >   name: cluster-viewer
    > subjects:
    >   - apiGroup: rbac.authorization.k8s.io
    >     kind: Group
    >     name: <group-name>
    > 
    > ```


**Related Information**  


[Kubernetes: Using RBAC Authorization](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)

[Kubernetes: Role Based Access Control Good Practices](https://kubernetes.io/docs/concepts/security/rbac-good-practices/)

[SAP Blogs: Using the Kubernetes-native Role-based access control](https://blogs.sap.com/2022/02/24/using-the-kubernetes-native-role-based-access-control/)

[Assign Roles in the Kyma Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/148ae38b7d6f4e61bbb696bbfb3996b2.html "Kyma uses roles to manage access within the cluster, which give the assigned users the permissions suitable for their purposes.") :arrow_upper_right:

[Cloud Foundry, Kyma, or Both?](cloud-foundry-kyma-or-both-ec8a269.md "You can set up one or more subaccounts that run both Cloud Foundry and Kyma, so that they can share SAP BTP services, such as SAP HANA Cloud. However, if your account model needs more complexity than just development stages, it's recommended to create one or more subaccounts specifically for Kyma, which can be shared between your teams.")

