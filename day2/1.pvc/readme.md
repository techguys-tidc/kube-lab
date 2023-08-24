# LAB PVC
In this lab, we will create a PVC named 'nginx-pvc-rwo' and a deployment named 'nginx-pvc' along with a configmap. This setup represents writing data to the PVC. After you've created these objects, try to delete the pod. You will observe that the 'index.html' file still persist even after the pod is deleted

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

### 1. Create the PVC.
Please copy file 1-pvc.yml and apply to your namespace.
```
kubectl apply -f 1-pvc.yml
```
Get PVC to see pvc in your namespace.
```
kubectl get persistentvolumeclaims
```
Short command.
```
kubectl get pvc
```
See verbose output
```
kubectl describe pvc <pvc-name>
```
Get pvc's YAML
```
kubectl get pvc <pvc-name> -o yaml
```


### 2. Create deployment.
Please copy file 2-deployment.yml and apply to your namespace.
```
kubectl apply -f 2-deployment.yml

```
Test how deployment persist data.
```
kubectl get pod
kubectl exec -it <pod-name> -- bash -c "echo Hi! > /usr/share/nginx/html/index.html"
```
Try to delete pod which are created from deployment and see what's happen?
```
kubectl delete pod <pod-name>
```
```
kubectl exec -it <pod-name> -- bash -c "cat /usr/share/nginx/html/index.html"
```

Test your application with port-forword.
```
kubectl port-forward <pod-name> 8000:80

and then open your browser access http://localhost:8000 or http://127.0.0.1:8000
```
Try to delete the pod to see what happen and try to test app again.
```
kubectl delete pod <pod-name> 
```


## Task
1. After you finish this lab Please capture screen or copy your result and put to the google sheet.
2. When you delete the pod, the content of the 'index.html' page will change to a different page?
