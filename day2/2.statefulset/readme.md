# LAB STATEFULSET
In this lab, we will create StatefulSets (sts) and PVCs. Through this exercise, you will gain a clear understanding of how StatefulSets work.

Before you begin, Please check and do it in your namespace.

Change namespace 

```
kubectl config set-context --current --namespace=<namespace-name>
```
Check current namespace
```
kubectl config current-context

kubectl config view
```

### 1. Create the statefulsets.
Please copy file statefulset.yml and apply to your namespace.
```
kubectl apply -f statefulset.yml
```
Get statefulset to see statefulset in your namespace.
```
kubectl get statefulsets
```
Short command.
```
kubectl get sts
```
See verbose output
```
kubectl describe sts <sts-name>
```
Get sts's YAML
```
kubectl get sts <sts-name> -o yaml
```

### 2. Explore StatefulSets.
To see result of the statefulset.
```
kubectl get pod 
kubectl get pvc
```
Test how sts persist data.
```
kubectl exec -it <pod-name> -- bash -c "hostname > /usr/share/nginx/html/index.html"
```
Try to delete pod which are created from sts and see what's happen?
```
kubectl delete pod <pod-name>
```

```
kubectl exec -it <pod-name> -- bash -c "cat /usr/share/nginx/html/index.html"

or access via browser

kubectl port-forward <pod-name> 8001:80

and then open your browser access http://localhost:8001 or http://127.0.0.1:8001
```



## Task
3. What is sts name?
4. What are pods name?
5. How many replicas in this statefulset?
6. What is the name of the StorageClass that this StatefulSet uses?