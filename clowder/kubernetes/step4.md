First we need to make sure all the pre-requisites are met to run clowder in kubernetes using HELM.

The helm chart assumes version 3 of helm. Lets make sure we have the right version:
`helm version`{{execute}}

Next we want to make sure kubernetes is ready and at least version 1.14
`kubectl get nodes`{{execute}}

Finally, we want to make sure a storageclass is defined
`kubectl get storageclass`{{execute}}


```
helm repo add ncsa https://opensource.ncsa.illinois.edu/charts
```{{execute}}

`helm install clowder ncsa/clowder --set commKey=katacoda`{{execute}}

`kubectl port-forward --address 0.0.0.0 --namespace clowder svc/clowder 9000:9000`{{execute}}

Render port 9000: https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com/
