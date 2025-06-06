# K8s

**What is Kubernetes ?**

 - Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications.

 - Developed by Google and now maintained by the Cloud Native Computing Foundation (CNCF) and released as open-source in 2014.

 - Kubernetes helps manage and organize containers automatically, ensuring that your containers keep running, can scale up when there's more traffic, and can move to healthy machines if something goes wrong.


🚀 **Why Use Kubernetes?**

Imagine you have an app running in a Docker container. Now, imagine you need to run 100 containers across 10 servers, handle failures, scale them up/down, manage load balancing, and update them without downtime. That's where Kubernetes shines.

<hr>

🧱 **Kubernetes Core Concepts**

1. *Cluster* - Cluster is group of master node and worker node
  - Master Node (Control Plane) – brain of the cluster, manages everything.
  - Worker Nodes – where your containers actually run.

2. *Pod* - The smallest unit in Kubernetes.
  - A pod can contain one or more tightly coupled containers.
  - All containers in a pod share networking and storage.

3. *Node*
 - A physical or virtual machine that runs your applications (pods).
 - Every node has a Kubelet (agent), container runtime (like Docker/Containerd), and Kube-proxy.

4. *Deployment*
 - Manages the desired state for your pods (e.g., number of replicas).
 - Handles updates, rollbacks, and ensures the app stays healthy.

5. *Service* - Provides a stable IP and DNS name to a set of pods. <br>
 *Types:*
   - ClusterIP (default) – for internal communication.
   - NodePort – exposes service on a static port on each node.
   - LoadBalancer – exposes service externally via cloud load balancer.

6. *Namespace*
 - Used to logically separate resources in the same cluster (multi-team or multi-project setup).

<hr>

