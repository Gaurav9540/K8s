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

<img src="assests/k8s-architecture.webp" alt="assests/k8s-architecture.webp" >

⚙️ Kubernetes Control Plane Components: 

 *API Server*  - 	Frontend to Kubernetes. All requests go through this.  <br>
 *Scheduler* - 	Assigns pods to suitable nodes based on resource requirements.  <br>
 *Controller Manager* - 	Ensures cluster state matches the desired state (e.g., ReplicaSet controller).  <br>
 *etcd* - 	Distributed key-value store for storing cluster data/configuration.  <br>


 🔧 Components of Worker Node:
 
 *1. Kubelet*
 - Talks to the API server on the control plane.
 - Receives PodSpecs and ensures the containers described are running and healthy.
 - Monitors the state of the pods and reports back to the control plane.   <br>
📌 Think of it as the node-level manager for containers.

*2. Container Runtime*
 - Responsible for pulling container images, starting, stopping, and managing container lifecycles.
 - Common runtimes:
   - containerd (default for modern K8s)
   - CRI-O
   - Docker (deprecated as of K8s v1.24+)  <br>
📌 Kubernetes uses a Container Runtime Interface (CRI) to talk to these runtimes.

 *Container Runtime* -	Software that runs containers (e.g., Containerd, Docker, CRI-O).  <br>
 *Kube-Proxy* - 	Maintains network rules and load balancing for service communication across pods and nodes.  <br>
 *Pods* -	The actual group of one or more containers running on the node.  <br>
