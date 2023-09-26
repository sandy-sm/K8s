Taints

* Applied on nodes to specify which nodes can be run on this node by scheduler
* Master node has a taint which allows not to schedule any user service pods


Tolerations

* Applied on pods to specify toleration for respective taints
* Once both taints and tolerations are applied on node and pods respectively. Scheduler schedules the pods on
the nodes


Tains - node

> kubectl taint nodes node-name key=value:taint-effect

where, taint-effect is one of [NoSchedule | PreferNoSchedule | NoExecute]


Tolerations:

```
apiVersion: 
kind: Pod
metadata:
    name: my-app-pod
spec:
    containers:
    -   name: nginx-container
        image: nginx
    tolerations:
    -   key: "app"
        operator: "Equal"
        value: "blue"
        effect: NoSchedule

```


- Scheduler can schedule a pod having toleration to taint in node. But it is not guaranteed 
- To restrict pod to allow only at given node, we would choose session affinity
- To restrict any pod to certain node, taint and toleration would be helpful
- E.g. not allowing any pod to run on master node (by defining taint)

Command to remove taint from node or untaint it.

> k taint nodes docker-desktop app=worker:NoSchedule-





