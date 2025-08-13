# Deployments

when creating similar pods of one types, you mostly require to create a Deployments. It creates a given number of replicas for the provided pod configurations and makes sure that these pods will be running.

A user creates a deployment, the deployment creates replicasets and these replicasets then create pods.

The deployment-controller in the kubernetes-control-manager manages the replicasets and the replicaset-controller allows you to make sure that any given position of time, your number of replica-count remains as specified.

## Properties of ReplicaSets

- Self Healing
- used in Rolling updates
- used in case of smooth transitions

---

### command Line interface

inorder to create a replica set via CLI you need to run the following command

```
    kubectl create deployment --name <replicaset_name> --image=<image_name> --port=<port> --replicas=<replica>
```

---

## Applying the Deployments

```
    Kubectl apply -f deployments.yml
```
