Create a new Deployment called nginx-deploy, with:

One container called nginx
Image: nginx:1.16
4 replicas
RollingUpdate strategy with:
maxSurge=1
maxUnavailable=2
Upgrade the Deployment to version 1.17.

Once all pods are updated, undo the update and roll back to the previous version.