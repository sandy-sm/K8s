
Two types of service account: User and Service

* User account
  * Any developer or admin accessing and using the cluster

* Service account
  * Any application accessing an dusing the cluster

    
> k create service-account dashboard-sa


> k get serviceaccount


> k describe serviceaccount dashboard-sa
-- It creates a secret object which contains the token
Tokens: dashboard-sa-token-sbdm

> k describe secret dashboard-sa-token-sbdm


token: ey.....lks


default service account each pod is attached 

current default token is not audience bound and is not time bound

v1.22 - Token API

v1.24 - when you create serviceaccount, it no longer creates token. we have to create the secret token 


Security enhancements:

KEP-1205
KEP-2799