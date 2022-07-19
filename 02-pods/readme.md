kubectl create ns wso2-training

kubectl run --image nginx nginx-pod --port 80
kubectl get pods

kubectl run --image nginx nginx-pod --port 80 -o yaml --dry-run=client > pod.yaml
kubectl apply -f pod.yaml

kubectl explain pod.spec.containers.resources

kubectl create deployment nginx --image nginx --port 80 -o yaml --dry-run=client > deploy.yaml

kubectl explain pod.spec == deploy.spec.template.spec

kubectl exec -it nginx-576785f88f-wl5nh -- /bin/sh

kubectl port-forward nginx-576785f88f-wl5nh 8080:80

kubectl exec -it nginx-576785f88f-wl5nh -- /bin/sh
cd usr/share/nginx/html
echo "hello world " >> index.html

kubectl delete all --all
