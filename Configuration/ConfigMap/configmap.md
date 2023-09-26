ConfigMap:

Grouping environment variables

> k create configmap app-config --from-literal=APP_COLOR=blue -n ckad


> k create configmap -n ckad --from-file=configmap.yaml


