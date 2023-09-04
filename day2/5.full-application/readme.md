# LAB challenge
In this lab, consist of pacman.yml and try-it.yml.

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

### 1. pacman 
Please copy file pacman.yml and apply to your namespace.
```
kubectl apply -f pacman.yml
```
Change ingress host to your desired name. Example [your_name]-pacman.training.dnsfor.me:2080

![image](https://github.com/techguys-tidc/kube-lab/assets/110895328/3ec31b42-c755-4193-982b-e21480a473e5)




### 2. try-it.
This file contains elements that need fixing in order to run the application. Your task is to troubleshoot and modify the file until the application can be executed successfully. Once you have managed to run the application without errors, proceed to access it and observe the results.
