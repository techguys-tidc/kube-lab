# LAB DAEMONSETS
In this lab, we will create daemonsets (ds). Through this exercise, you will gain a clear understanding of how daemonsets work.

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

### 1. Create the daemonsets.
Please copy file daemonsets.yml and apply to your namespace.
```
kubectl apply -f daemonsets.yml
```
Get daemonsets to see daemonsets in your namespace.
```
kubectl get daemonsets
```
Short command.
```
kubectl get ds
```
See verbose output
```
kubectl describe ds <pvc-name>
```
Get ds's YAML
```
kubectl get ds <pvc-name> -o yaml
```

### 2. Explore daemonsets.
To see result of the daemonsets.
```
kubectl get pod -o wide
```
Try to delete pod which are created from sts and see what's happen?
```
kubectl delete pod <pod-name>
```


## Task
7. What nodes are pods place in?
8. Show result of ds

