Create a pod named time-check in the dvl1987 namespace. This pod should execute a container called time-check using the busybox image.

Create a ConfigMap named time-config with the data TIME_FREQ=10 in the same namespace.
The time-check container must run the command: while true; do date; sleep $TIME_FREQ; done, directing the output to the file located at /opt/time/time-check.log.
Ensure that the path /opt/time within the pod mounts a volume that persists for the duration of the pod's lifecycle.