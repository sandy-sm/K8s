#### Resource Limits

- kube-scheduler decides which pod will be assigned to which node based on availability of resources i.e. cpu, memory
- if no resources available kube-scheduler holds placing the pod onto node and it goes in pending state with reason insufficient cpu

units:
cpu: 1   --> 1 vCPU aws, 1 gcp core, 1 azure core, 1 hyperthread


memory : 
1 G = Gigabyte = 1,000,000,000 bytes (1B)
1 M = Megabyte = 1,000,000 bytes (1M)
1 K = Kilobyte = 1,000 (1K)

1 Gi = Gibibyte = 1,073,741,824 bytes 
1 Mi = Mebibyte = 1,048,576 bytes
1 Ki = Kibibyte = 1,024 bytes


-----------------

No Requests - No Limits --> default configuration - one pod may consume as much resources as it want.

No Requests - Limits --> requests = limits, 
pod will be restricted to the limit specified, resources gets wasted if pod 2 is not using it's full limit and pod 1 does.

Requests - Limits -> pod will be restricted and guaranteed minimum requests.

Requests - No Limits -> Pods will be guarenteed specified requests, if not limit specified it is flexible to use the system resources. optimal utilization of resources. 
but could be misused if given to public.


---------------





                    
