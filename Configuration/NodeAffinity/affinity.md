
the primary purpose is to schedule and execute the pod to the nodes.

provides advanced capabilities to place the pods on the nodes.

```
affinity:
    nodeAffinity:
        requiredDuringSchedulingIgnoredDuringExecution:
            nodeSelectorTerms:
            - matchExpressions
              - key: size
                operator: In
                values:
                  - Large
                  - Medium
```

Affinity types: Defines the behaviour of a scheduler

Available:
1) requiredDuringSchedulingIgnoredDuringExecution
2) preferredDuringSchedulingIgnoredDuringExecution

Planned
3) requiredDuringSchedulingRequiredDuringExecution


| Type   |During Scheduling|During Execution|Description|
|--------|-----|------|----|
| Type 1 |Required|Ignore|label should exist|
| Type 2 |Preferred|Ignore|no impact to running pod which already scheduled|
| Type 3 |Required|Required|running pod is evicted|





