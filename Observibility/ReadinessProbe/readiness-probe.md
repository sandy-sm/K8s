#### Pod readiness

* sometimes pod is not ready to accept user traffic even though it is in ready state
* k8s mark pod is ready as soon as application has kick-started but may not open the port until then it is a service disruption for user
* To avoid this, k8s provides readiness probe which is a specific condition on which it is ready to accept traffic
* Type of readiness probe:
  * HTTP test
  * TCP socket
  * exec command

##### HTTP Test

```
readinessProbe:
    httpGet:
        path: /api/ready
        port: 8080
```


##### TCP

```
readinessProbe:
    tcpSocket:
        port: 3306
```

#### Exec command

```
readinessProbe:
    exec:
        command:
            - cat
            - /app/is_ready

```



#### Additional delay

* if you know that application will take minimum 10 seconds to warm up. we can add initialDelaySeconds
* how often to probe: periodSeconds
* failureThreshold: number of failure retries

```
readinessProbe:
  httpGet:
    path: /api/ready
    port: 8080
  intialDelayInSeconds: 10
  periodSeconds: 5
  failureTheshold: 8
```