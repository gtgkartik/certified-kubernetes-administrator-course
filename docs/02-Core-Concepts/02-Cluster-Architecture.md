# Cluster Architecture

  - Take me to [Video Tutorial](https://kodekloud.com/topic/cluster-architecture/)

In this section , we will take a look at the kubernetes Architecture at high level.
- 10,000 Feet Look at the Kubernetes Architecture

  ![Kubernetes Architecture](../../images/k8s-arch.PNG)

## Notes from the Above image
Let's Think in terms of Kubernetes Architecture
Let's start with two things 

### 1. Master Node and Worker Node:
The Ship with Master Node is the master and it manages all the worker nodes,
a worker nodes will contain containers.

### 2. Kube Proxy 
The containers from one worker node will communicate with other container from another worker node
using this kube proxy.

### 3. Kubelet
Every worker node is operated and controlled by kubelet, think of this kubelet as a agent.

Now inside Master Node there are few components that we need to discuss

### 1. Controller manager 
This contains various managers like node controller that manages nodes and other controllers

### 2. ETCD
The infromation about what a controller manager should do will come from ETCD 

### 3. Kude scheduler 
What containers be assigned to what worker nodes depending upon worker avilability and capability is done by kube scheduler

### 4. Kube APi Server
the above 3 main core components inside the Master node will talk to each other with the help of the kube api server
  
  ![Kubernetes Architecture 1](../../images/k8s-arch1.PNG)

  

K8s Reference Docs:
- https://kubernetes.io/docs/concepts/architecture/
