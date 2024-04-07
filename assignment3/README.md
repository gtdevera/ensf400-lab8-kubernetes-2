# Initial Setup:

Start with:
```
minikube start
```
You will get this:

![image of output from minikube starting](pictures/minikube-start.png)

Make sure to run:
```
minikube addons enable ingress
kubectl apply -f ./
```
Ingress:

![image of output from ingress addon enabling](pictures/ingress-enable.png)

Outcome of the .yaml files:

![image of deployments, pods, and configmap being made](pictures/all-apply.png)

# Optional Debugging

Use the below for debugging:
```
kubectl describe pod pod_name
kubectl logs pod_name
```

# Check to See if it Worked

In order to see if the pods and deployments work run these commands:
```
kubectl get pods
kubectl get deployments
kubectl get configmaps
```
Result from getting pods:

![get pods result](pictures/get-pods.png)

Result from getting deployments:

![get deployments result](pictures/get-deps.png)

Result from getting configmaps:

![get configmaps result](pictures/get-configs.png)

# Running Curl

Make sure to run this command in order to get the ip of Minikube:
```
minikube ip
```
and then use this command for the curl:

```
curl http://<minikube ip>/
```

Here is the result from running the command multiple times

![results of curling multiple times](pictures/curl-results.png)

# Deleting Pods, Deployments, etc.

Get rid of all resources
```
kubectl delete -f ./
```

Stop Minikube
```
minikube stop
```