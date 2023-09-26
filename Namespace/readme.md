### Theory

* Namespaces are used to arrange the resources in a single workspace
* Pods withing same namespace can call each other with direct name
* Pods who want to connect with other pods of different namespace would connect by
  * $pod-name. $namespace  .svc.cluster.local
  * E.g. db-service.dev.svc.cluster.local
* Each namespace can have it's own policies and resource quota limits


### Uses


### Commands

Using file

> k create -f namespace-dev.yaml

Alternatively,
> k create ns dev


To set the namespace as default

> k config set-context $(k config current-context) --namespace=dev


To apply resource quota to namespace

> k create -f resource-quota.yaml


To see pods of all namespaces

> k get po --all-namespaces

Alternatively,
> k get po -A


To access service / pod of another namespace use below DNS name

> $pod-name. $namespace  .svc.cluster.local

> $service-name. $namespace  .svc.cluster.local