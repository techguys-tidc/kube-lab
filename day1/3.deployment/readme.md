# Lab deployment

## task 1 Get Deployment

### To show deployment all namespace
```
kubectl get deployment -A 
```
### To show specific deployment (in this case deployment name is your name)
```
kubectl get deployment [DEPLOYMENT_NAME]
```

## task 2 Create deployment

```
kubectl create deployment [DEPLOYMENT_NAME] --image nginx --replica 1
```
## task 3 Describe deployment

```
kubectl scale deployment [DEPLOYMENT_NAME] --replica 2
```

## task 4 Describe deployment

```
kubectl describe deployment [DEPLOYMENT_NAME]
```

## task 5 Delete deployment 
```
kubectl delete deployment [DEPLOYMENT_NAME]
```

## task 5 Create deployment using manifast

```
kubectl apply -f deployment.yaml
```

## Please answer the questions (put your answer to google sheet).

 6. Show result after scale deployment.
 7. After Create deployment using manifast, How many pod which come form the same deployment ?
 8. After Create deployment using manifast, What is lable attached to this deployment ?