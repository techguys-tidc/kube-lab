# LAB NETWORK
In this lab, we will enjoy about kubernetes networking. Through these exercise, you will gain a clear understanding of kubernetes networking.

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

### 1. Create the deployment.
Please copy file 1-deployment.yml and apply to your namespace.
```
kubectl apply -f 1-deployment.yml
```
Get deployment to see deployment in your namespace.
```
kubectl get deployments
```
Short command.
```
kubectl get deploy
```
See verbose output
```
kubectl describe deployments <deployment-name>
```
Get deployment's YAML
```
kubectl get deployments <deployment-name> -o yaml
```
You can see the application run now but how can we access to our application without kubectl port-forword.

### 2. Create service.
Please copy file 2-service.yml and apply to your namespace.
```
kubectl apply -f 2-service.yml
```
Get service to see services in your namespace.
```
kubectl get services
```
Short command.
```
kubectl get svc
```
See verbose output
```
kubectl describe svc <svc-name>
```
Get svc's YAML
```
kubectl get svc <svc-name> -o yaml
```
'kubectl get services' this command will give you the list of services name, service ip and services port.

### 3. Create ingress.
Copy file 3-ingress.yml and apply to your namespace.

Edit host name in 3-ingress.yml
```
your_name.training.dnsfor.me
```

Before apply file 3-ingress.yml, please change host (nginx-lab-network.poc.workisboring.com) to your domain name.
```
kubectl apply -f 2-ingress.yml
```
Get service to see ingress in your namespace.
```
kubectl get ingresses
```
Short command.
```
kubectl get ing
```
See verbose output
```
kubectl describe ing <ing-name>
```
Get ing's YAML
```
kubectl get ing <ing-name> -o yaml
```
'kubectl get ingresses' this command will give you the list of host, addresses.


After Create all objects Test you application.

Access your domain.
Example 
nginx-lab-network.poc.workisboring.com 


