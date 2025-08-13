# Kubernetes Cluster creation

A kubernetes cluster is nothing but a combination of both your worker nodes and your kubernetes control panel

## Kubernetes Control Panel (Master Node)

A Kubernetes master node contains five major k8s component which powers kubernetes.

- Kubernetes API Server - the api http server with which the developer interact for pod creations
- Kubernetes etcd - a fast key value pair that k8 uses to store all the api data
- Kubernetes controller manager - a control loop that runs and check if everything in container is running as per the kubernetes configuration
- Kubernetes Scheduler - which controls where the next pod, or in which node the next pod needs to be assigned
- Cloud Control Manager - a control manager which is used to interact with cloud apis for your kubernetes cluster

## Kubernetes Worker Node

A worker node is like a machine which runs your group of processes - pods

- Kubelet - A kubelet is basically the on-node �agent� in Kubernetes � the little worker program that makes sure your node is doing what the Kubernetes control plane told it to do.
- KubeProxy - a network controller for your worker node.

---

To create a k8 cluster you use Kind and apply its config or use cmd

create k8 using CLI for single node cluster

```
    kind create cluster --name <cluster_name >
```

creating a multi-node setup usually requires a yml file which you can provide and apply in the following way

```
kind create cluster --config <filename>.yml --name <cluster_name >
```

## Checking cluster creation

you can check if your cluster was created properly via Kubectl and check the total running nodes.

```
    kubectl get nodes

```
