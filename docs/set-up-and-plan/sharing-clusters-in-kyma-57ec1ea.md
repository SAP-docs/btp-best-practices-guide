<!-- loio57ec1ea5ca3b4cdeb5f60453b91058af -->

# Sharing Clusters in Kyma

Sharing a Kyma cluster among multiple teams, applications, or in partner scenarios, can improve efficiency with regard to cost, administration, and rule enforcement. However, before you set up cluster sharing, carefully consider your specific use case to ensure optimal security, isolation, and resource allocation.

The following recommendations help you decide whether sharing a cluster is a good option for you and provide best practices and effective mitigation actions, based on [Kubernetes: Multi-tenancy](https://kubernetes.io/docs/concepts/security/multi-tenancy/).



<a name="loio57ec1ea5ca3b4cdeb5f60453b91058af__section_qxw_dgj_w1c"/>

## Use Cases

You must understand and define the objectives and expected outcomes for your specific use case. Typical reasons for cluster sharing include cost optimization, resource utilization, and collaboration between teams. The following use cases are common:



### Multiple Customers

This use case is typical if you want to serve several external customers \(for example, in a partner scenario\). The customers don't have access to the cluster; Kubernetes is invisible from their perspective and is only used by the vendor to manage the customer workloads. You must ensure that the workloads are strictly isolated from each other.

> ### Caution:  
> It's not recommended to share the cluster among multiple customers. Instead, use separate clusters to ensure strict isolation of the users' workloads, guarantee absolute fairness on all levels, and prevent manipulations.



### Multiple Teams

Members of the teams often have direct access to Kubernetes resources using tools. Typically, there is some level of trust between members of different teams, but you must apply Kubernetes policies such as role-based access control \(RBAC\), quotas, and network policies to safely and fairly share clusters.

For multiple teams, cluster sharing \(with the respective mitigations\) is useful in the following scenarios:

-   Small teams or applications: If you have a small number of teams or applications with low resource requirements, sharing a cluster can maximize resource utilization and reduce infrastructure costs.

-   Development and testing environments: Sharing a cluster is often acceptable for development and testing purposes. These environments typically have lower security and isolation requirements, making it easier to share resources. For more information, see [Staged Development with the Kyma Environment](staged-development-with-the-kyma-environment-ec8a269.md).

-   Non-critical workloads: If the workloads running on the cluster are non-critical or have a low impact on business operations, sharing a cluster can be a viable option. This is especially true for non-production environments or temporary projects.




<a name="loio57ec1ea5ca3b4cdeb5f60453b91058af__section_lgm_vgj_w1c"/>

## Checklist for Shared Clusters

Consider the following mitigative actions for the control plane and data plane:



### Control Plane Isolation

Control plane isolation ensures that different tenants cannot access or affect each others' Kubernetes API resources. The control plane manages the Kubernetes resources, enforces access to those, and prevents tenants from viewing, creating, editing, or deleting objects in another tenant. The control plane also manages global resources that affect the entire cluster. To isolate tenants from the impact of changes to global resources, consider the following mitigative actions:

-   Use namespaces for isolation.

    Kubernetes provides [namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/) as a logical grouping mechanism. Each team or user can have their own namespace, which isolates the groups of API resources within a single cluster.

-   Use RBAC to control their access to resources and scope them to their respective namespaces.

    Implement RBAC to manage user access and permissions within the cluster. Assign appropriate roles and permissions to ensure that users have the necessary access without compromising security. See [Role-Based Access Control \(RBAC\) in Kyma](role-based-access-control-rbac-in-kyma-bb31080.md).

-   Cluster admins manage global resources and Custom Resource Definitions \(CRDs\).

    Global resources are outside of the namespace concept and must be managed by administrators. They are applied to all “tenants” in the same way and updates affect everyone at the same time. While this is limiting, there are several benefits: It incentivizes teams to use the same tools without needing to operate them, keeps the versions consistent across teams, and encourages that global best practices are provided or even enforced.

-   Use policies for compliance.

    Use policy engines, like [Gatekeeper](https://open-policy-agent.github.io/gatekeeper/website/docs/howto/) or [Kyverno](https://kyverno.io/), to enforce policies on what “tenants” can and cannot do. In addition, these policy engines can add metadata, like labels, to every workload tagging it with the “tenant” name for easier filtering of logs.

-   Use quotas, limits, and priorities for controlling resource allocation.

    To control how many resources a tenant can occupy, especially in clusters that have a limited ability to scale, it's recommended to set [resource quotas](https://kubernetes.io/docs/concepts/policy/resource-quotas/) for tenants. Also, use resource quotas to limit the maximum resources of Pods, to assure that they fit on nodes besides the global workload.

    > ### Example:  
    > If a node has 64GB of RAM and the "global tooling" needs 4GB, the Pod size must be limited to 60GB of RAM; otherwise, the Pods cannot be scheduled reliably or run the risk of being evicted frequently.

    If multiple namespaces are supported, you must establish a way to limit the consumption across multiple namespaces using [limit ranges](https://kubernetes.io/docs/concepts/policy/limit-range/). Similarly, restrict the [Pod priorities](https://kubernetes.io/docs/concepts/scheduling-eviction/pod-priority-preemption/) that can be set in a specific tenant, for example, prioritizing production workloads over background batch jobs.




### Data Plane Isolation

Data plane isolation ensures that workloads from one tenant cannot interfere with workloads from another tenant. Two primary domains of isolation are networking and storage. However, you can use additional measures to prevent breached workloads from affecting other tenants of the same cluster.

-   Define network policies to control traffic flow.

    Implement network policies to control traffic flow between different namespaces or applications. This helps enforce security and isolation and prevents unauthorized access or interference.

-   Use centralized observability.

    To track cluster-wide resource usage, performance metrics, and health, implement a centralized observability solution that the tenants can access and filter for their data. Ideally, access can be restricted to the tenants' data only.

-   Use Istio with dedicated ingress gateways.

    Istio, an open source service mesh, improves traffic shaping and supports mTLS between the Pods, securing the traffic even more against other tenants sniffing traffic. Use dedicated ingress gateways per tenant to configure the domains individually. For details, see [Istio Module](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/26ffe00c24574db58697992b93f397ac.html "Use the Istio module to manage and configure the Istio service mesh.") :arrow_upper_right:.


