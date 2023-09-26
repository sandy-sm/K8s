

> k get po <pod-name> -o yaml > existing-pod.yaml

Modify existing-pod.yaml


> k apply -f existing-pod.yaml


> k replace --force -f /tmp/edited-pod.yaml


