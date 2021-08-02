# mongodb on Kubernetes setup
Check the official page here https://github.com/mongodb/mongodb-kubernetes-operator

Just playaround with the deployment of MongoDB on Kubernetes.

Prerequisites:

- GCP environment is ready
- GKE - Google Kubernetes Engine cluster is ready

Works:

- Can execute to insert/update/delete documents in Mongodb.
- Can scale up/down the number of Mongodb instances.
- Delete the MongoDB Community Kubernetes Operator would not clean up the PV/Gcloud Disks.
- Delete the Kubernetes namespaces can clean up everything.

Some open points:

- How to do the manually backup? Is it possible with the MongoDB Community Kubernetes Operator?
- How to increase the persistent volume size (current: the data volume is set to 10Gb, log volume is 2Gb)?

## Using MongoDB Community Kubernetes Operator

```
# Run the following command to create cluster-wide roles and role-bindings
kubectl apply -f 0_dev_namespace.yaml
kubectl -n dev apply -f 1_mongodbcommunity.mongodb.com_mongodbcommunity.yaml
kubectl -n dev apply -f 2_rbac/
kubectl -n dev apply -f 3_manager.yaml
kubectl -n dev apply -f 4_mongodb.com_v1_mongodbcommunity_cr.yaml
```


### Install MongoDB Resource

```
kubectl apply -f config/samples/mongodb.com_v1_mongodbcommunity_cr.yaml

```

### Rollback all

```
kubectl delete namespaces dev
```

### Mongodb console:

```
mongo admin -u mongoadmin

enter your password

db.inventory.insertOne(
   { item: "canvas", qty: 100, tags: ["cotton"], size: { h: 28, w: 35.5, uom: "cm" } }
)

db.inventory.insertMany([
   { item: "journal", qty: 25, tags: ["blank", "red"], size: { h: 14, w: 21, uom: "cm" } },
   { item: "mat", qty: 85, tags: ["gray"], size: { h: 27.9, w: 35.5, uom: "cm" } },
   { item: "mousepad", qty: 25, tags: ["gel", "blue"], size: { h: 19, w: 22.85, uom: "cm" } }
])

db.inventory.find( {} )
```
