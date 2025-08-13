# ReplicaSets

when creating similar pods of one types, you mostly require to create a replicaSet. It creates a given number of replicas for the provided pod configurations and makes sure that these pods will be running.

The replicaset-controller in the kubernetes-control-manager allows you to make sure that any given position of time, your number of replica-count remains as specified.

## Properties of ReplicaSets

- Self Healing

---

### command Line interface

inorder to create a replica set via CLI you need to run the following command

```
    kubectl create rs --name <replicaset_name> --image=<image_name> --port=<port> --replicas=<replica>
```

---

## Applying the ReplicaSet

```
    Kubectl apply -f replicaset.yml
```
