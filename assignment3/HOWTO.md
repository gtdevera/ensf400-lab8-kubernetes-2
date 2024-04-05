Start with:
```
minikube start
```

make sure to run:
```
minikube addons enable ingress
kubectl apply -f ./
```


Use the below for debugging:
```
kubectl describe pod pod_name
kubectl logs pod_name
```

Get rid of all resources
```
kubectl delete -f ./
```

Stop Minikube
```
minikube stop
```