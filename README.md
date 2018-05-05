# Kubernetes Study Guide
This project is just a few things that I learned studying kubernetes.

## kubectl get pods \<pod name>

Return what is running on this pod.

## kubectl attach \<pod name> -c \<container>

Enter into the running container in the specified pod.

## kubectl label [--overwrite] \<type> KEY=VALUE ...

Set a label to a pod.

## kubectl exec [it] \<pod name> [-c CONTAINER] --COMMAND [args...]

Exec (iterative or not) a command into the container (such like docker exec -it \<contaier> bash).

## kubectl run \<name> --image=image

Run a docker image in an easy way.

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