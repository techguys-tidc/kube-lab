# Lab namespace


## task 1 Get namespace 

#### To show all namespace in this cluster
```
kubectl get namespace 
```
#### To show specific namespace (in this case namespace name is your name)
```
kubectl get namespace [NAMESPACE_NAME]
```

## task 2 Create namespace
```
kubectl create namespace [NAMESPACE_NAME]
```

## task 3 Describe namespace
```
kubectl describe namespace [NAMESPACE_NAME]
```

## task 4 Delete namespace 
```
kubectl delete namespace [NAMESPACE_NAME]
```

## task 5 Create namespace using manifast

```
kubectl apply -f namespace.yaml
```

## Please Answer the questions (put your answer to google sheet).
 1. Before you create your namespace, How many namespace in this cluster ?	
 2. Show result when you run command "kubectl get namespace [NAMESPACE_NAME]"