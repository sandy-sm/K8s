
A secret in k8s allows to keep sensitive data like passwords in non-plain text format

two steps
1) create a secret
2) inject into pod

> k create secret generic <secret-name> --from-literal=<key>=<value>


OR

> k create secret generic <secret-name> --from-file=<path-to-file>


#### Notes

* Secrets are not encrypted. they are encoded   
* secrets are not encrypted in ETCD
* kind: EncryptionConfiguration
* secret storage provider: aws, azure, gcp, harshicorp vault

Demo on encrypting secrets at rest:
https://www.udemy.com/course/certified-kubernetes-application-developer/learn/lecture/34549240#reviews

