At this point we are ready to start clowder using Helm using the previously configured values.

```
helm install clowder ncsa/clowder --values katacoda.yml
```{{execute}}

This command will start all parts of clowder, and add a single user to clowder. To check the progress use

```
kubectl get pods -w
```{{execute}}

Once all pods are ready, clowder has started and you can use `^C`{{execute ctrl-seq}} to stop.
