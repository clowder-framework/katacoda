Normally we will have clowder configured with an ingress route and the helm chart will add all required pieces to make clowder reachable at the specified URL.

In this case we do not have an ingress route specified (since there is no ingress controller running). We can, however, use port forwarding to make the application reachable.

```
kubectl port-forward --address 0.0.0.0 svc/clowder 9000:9000
```{{execute}}

Clowder can now be seen at https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com/
