# Kubernetes Architecture

Kubernetes is a container orchestration platform used to manage containers. It offers several advantages, such as scalability, self-healing capabilities, and cluster management.

![K8s_architecture](https://github.com/ChaitanyaKMV/devops_learning/assets/19556341/8cdce7e5-b8c5-4ac9-8065-b18853c07360)


## Components of Kubernetes

### Control Plane (Master Node)

The Control Plane, often referred to as the Master Node, consists of the following components:

1. **API Server:** Acts as the entry point for the Kubernetes control plane and is responsible for serving the Kubernetes API.

2. **etcd:** A distributed key-value store that stores configuration data and serves as the cluster's source of truth.

3. **Controller Manager (CM):** Manages various controllers that regulate the state of the system, such as the ReplicaSet Controller and the Node Controller.

4. **Scheduler:** Assigns work (containers) to worker nodes, based on resource requirements and other constraints.

5. **Cloud Controller Manager (CCM):** Integrates the cluster with cloud provider-specific APIs. It allows Kubernetes to interact with cloud resources.

### Data Plane (Node)

The Data Plane, also known as the Node, consists of the following components:

1. **Kube-proxy:** Maintains network rules on nodes. It is responsible for forwarding traffic to the appropriate service, load balancing, and network policy enforcement.

2. **Kubelet:** Ensures that containers are running in a Pod. It communicates with the control plane to manage the containers.

3. **Container Runtime:** Kubernetes supports various container runtimes, such as Containerd and cri-o. This component manages the execution of containers.

## Summary

Understanding the Kubernetes architecture is crucial for effectively managing containerized applications. The Control Plane and Data Plane work together to maintain the desired state of the cluster and ensure the efficient operation of your workloads.

For more detailed information and in-depth explanations of each component, refer to the official [Kubernetes documentation](https://kubernetes.io/docs/concepts/architecture/).
