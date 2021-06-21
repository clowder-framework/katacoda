Now that we know that we have the pre-requisites to run clowder in Kuberentes, we can add the helm repository and make sure we have the latest helm chart information.

```
helm repo add ncsa https://opensource.ncsa.illinois.edu/charts
helm repo update
```{{execute}}

Lets check to make sure we can find clowder.

```
helm search repo clowder
```{{execute}}
