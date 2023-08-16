# Lab namespace

## task 1 Get Pod

### To show pod all namespace
```
kubectl get pod -A 
```
### To show specific pod (in this case Pod name is Your name)
```
kubectl get pod [POD_NAME]
```

## task 2 Create Pod

```
kubectl run [POD_NAME] --image nginx
```

## task 2 Describe Pod

```
kubectl describe pod [POD_NAME]
```

## task 4 Delete Pod 
```
kubectl delete pod [POD_NAME]
```

## task 5 Create Pod using manifast

```
kubectl apply -f pod.yaml
```

## Please Answer the questions (put your answer to google sheet).

 3. What namespace does the pod name 'traning' run?
 4. Show result after create pod with your name
 5. What image does the pod name 'nginx' use for run in your namespace and what container port number that it use? 