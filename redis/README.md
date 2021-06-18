# how to start the deployment?
## For the master slave approach | multiple instances of redis
kubectl apply -f redis-k8s-primary-slave.yaml

## For one single pod for redis instance