At this point we are ready to start clowder using Helm using the previously configured values.

```
helm install clowder ncsa/clowder --values katacoda.yml
```{{execute}}

This command will start all parts of clowder, and add a single user to clowder. To check the progress use

```
kubectl get pods -w
```{{execute}}

You will see pods get into running state, and eventually they will be ready. Most likely the last pod that will get into ready state is clowder. Once all pods are ready, clowder has started and you can use `^C`{{execute ctrl-seq}} to stop listing the pods.
