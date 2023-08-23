# StorageClass
For storageClass is a cluster-wide object in Kuberneter So We created the storageClass only once for each cluster. Sometimes, you might have multiple storageClasses within the cluster with unique names.

## This Lab will show you How to find the storageClass in the cluster.
To get the storageClass. You will see the list of storageClasses.
```
kubectl get storageclasses
```
For short command you can use.
```
kubectl get sc
```
To see detail of the each storageClass.
```
kubectl get sc <storageclass-name> -o yaml
```
In this cluster
```
kubectl get sc iscsi -o yaml
```