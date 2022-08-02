kubectl get pods -o wide

kubectl expose deploy/nginx --port 80 --target-port 80 -o yaml --dry-run --type=ClusterIP> service.yaml

kubectl run -it --image busybox:1.28 busybox --rm -- /bin/sh

<service-name>.<namespace>.svc.cluster.local

if service is in a different namespace
<service-name>.<namespace>.svc
if all are in same namespace
<service-name>

kubectl expose deploy/nginx --port 80 --target-port 80 -o yaml --dry-run --type=NodePort> service-np.yaml
