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

Katacoda does not have a default storage class, before starting clowder, lets create some persistent volumes that we will use later.

```
# create pv
kubectl apply -f pv.yml
# case of 1 node cluster
mkdir -p /root/volumes/{clowder,elasticsearch,mongodb,rabbitmq}; chmod 777 /root/volumes/*
# case of 2 node cluster
ssh node01 'mkdir -p /root/volumes/{clowder,elasticsearch,mongodb,rabbitmq} ; chmod 777 /root/volumes/*'
```{{execute}}


At this point we have a kubernetes cluster that can run clowder.
