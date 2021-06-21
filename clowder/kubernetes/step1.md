Before we begin, we should check to make sure kubernetes is up and running. This is specific to katacoda, and will wait until the kubernetes cluster has started.

```
launch.sh
```{{execute}}

Once kubernetes is running we can look a the cluster (cluster will have a single node).

```
kubectl get nodes
```{{execute}}

The clowder helm chart needs helm version 3
```
helm version
```{{execute}}

At this point we have a kubernetes cluster that can run clowder.
