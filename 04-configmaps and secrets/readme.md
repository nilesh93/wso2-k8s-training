kubectl create deploy --image nginx nginx --port 80 -o yaml --dry-run > deploy.yaml
kubectl expose deploy nginx --port 80 --target-port 80 --dry-run -o yaml > svc.yaml

kubectl create cm app-config --from-literal hello=world -o yaml --dry-run > app-config-cm.yaml

/usr/share/nginx/html/index.html

kubectl create cm index-html --from-file=./index.html -o yaml --dry-run >index-html-cm.yaml
