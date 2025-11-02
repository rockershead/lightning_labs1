Create a PersistentVolume named log-volume with the following specifications:

StorageClassName: manual (already created for you — do not create it again)
AccessModes: ReadWriteMany (RWX)
Capacity: 1Gi
hostPath: /opt/volume/nginx
Next, create a PersistentVolumeClaim named log-claim that:

Requests at least 200Mi of storage
Binds to the log-volume created above
Finally, create a pod named logger that:

Uses the image nginx:alpine
Mounts the log-claim at the path /var/www/nginx inside the container