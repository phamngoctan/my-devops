# mongodb on Kubernetes setup

## Using MongoDB Community Kubernetes Operator

```
git clone https://github.com/mongodb/mongodb-kubernetes-operator.git

# Run the following command to create cluster-wide roles and role-bindings
kubectl apply -f deploy/clusterwide

# Install the necessary roles and role-bindings
kubectl apply -k config/rbac


# Install the Custom Resource Definitions
kubectl apply -f config/crd/bases/mongodbcommunity.mongodb.com_mongodbcommunity.yaml
kubectl get crd/mongodbcommunity.mongodbcommunity.mongodb.com

# Verify that the resources have been created
kubectl get role mongodb-kubernetes-operator

kubectl get rolebinding mongodb-kubernetes-operator

kubectl get serviceaccount mongodb-kubernetes-operator

# Install Operator

kubectl create -f config/manager/manager.yaml
kubectl get pods

```


### Install MongoDB Resource

```
kubectl apply -f config/samples/mongodb.com_v1_mongodbcommunity_cr.yaml

```

### Rollback all

```
kubectl delete -f config/samples/mongodb.com_v1_mongodbcommunity_cr.yaml
kubectl delete -f config/manager/manager.yaml
kubectl delete -f config/crd/bases/mongodbcommunity.mongodb.com_mongodbcommunity.yaml
kubectl delete -k config/rbac
kubectl delete -f deploy/clusterwide

```

## Using MongoDB Community Kubernetes Operator

