A cluster can have nodes of various hardware sizes.

The more the hardware size of a node, the more pod size (in terms of memory/cpu requirements) it can host.

We can define a nodeSelector in the spec of pod yaml file with label key/value.

The same label key/value is configured to node.

We can label the node using below command:

> k label nodes node-1 key=value


Limitation:

we cannot use complex conditions with Node selector such as medium or large, not small etc.

Hence, node affinity is used

