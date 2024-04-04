Start with:
```
minikube start
```

make sure to run:
```
minikube addons enable ingress
kubectl apply -f nginx-dep.yaml
kubectl apply -f nginx-configmap.yaml

kubectl apply -f app-1-dep.yaml
kubectl apply -f app-2-dep.yaml
```


Use the below for debugging:
```
kubectl describe pod pod_name
kubectl logs pod_name
```

```
kubectl delete deployments --all
kubectl delete pods --all
```

```
minikube stop
```