Create a deployment in the default namespace with the following specifications:

Name: redis
Image: redis:alpine
Replicas: 1
Labels: app=redis
CPU Request: 0.2 CPU (200m)
Container Port: 6379
Volumes:

An emptyDir volume named data, mounted at /redis-master-data.
A ConfigMap volume named redis-config, mounted at /redis-master.
The ConfigMap has already been created for you. Do not create it again.
Note: All resources should be created in the default namespace (unless specified otherwise).