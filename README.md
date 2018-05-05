# Kubernetes Study Guide
This project is just a few things that I learned studying kubernetes.

## kubectl expose

|Parameter|Description|
|----|-----------|
|`--type`|NodePort = map a single port port to a single node|
|        |LoadBalancer = map a single port to N ports |

**NodePort** example: `kubectl expose deployment tomcat-deployment --type=NodePort`

**LoadBalancer** example: `kubectl expose deployment tomcat-deployment --type=LoadBalancer --port=8080 --target-port=8080 --name=tomcat-load-balancer`

## kubectl describe

Returns information about anything, pods, load balancer, etc.

E.g: `kubectl describe service tomcat-load-balancer`