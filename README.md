### `start`
minikube start
kubectl apply -f ns-indrakila.yaml
kubectl apply -f configmap-indrakila.yaml -n development
kubectl apply -f indrakila.yaml -n development
kubectl apply -f ingress-indrakila.yaml -n development
minikube service indrakila --url -n development
minikube ip
vim nano /etc/hosts
<ip-minikube>  <url from inggres>



### `enable ingress controller in minikube`
minikube addons enable ingress

### `create expose service in minikube`
minikube service <name> --url
minikube service indrakila --url -n development


### `create namespace`
kubectl create ns development

### `start yaml`
kubectl create -f indrakila.yaml -n development

### `apply yaml`
kubectl apply -f indrakila.yaml -n development

### `restart deployment`
kubectl rollout restart deployment indrakila -n development

### `describe`
kubectl describe deployment indrakila -n development

### `pod`
kubectl get pod -n development

### `Expose`
kubectl expose deployment indrakila --port=5001 --target-port=5000

### `logs`
kubectl logs <pod> -n development

### `nodes`
kubectl get nodes

### `create secret manual`
echo -n `string` | base64

kubectl port-forward -n development


### `edit /etc/hosts`
sudo vim /etc/hosts
ip-address url

### `checking error`
kubectl describe pod <name-pod> -n development
