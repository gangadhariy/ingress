<h1 allign="center">HOW TO INSTALL NGINX INGRESS CONTROLLER</h1>

## Follow the instructions 

## First you need to install nginx ingress.

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.1/deploy/static/provider/baremetal/deploy.yaml
```


It will create a namespace named ingress-nginx and deploy some pods within it. Among these pods, two will have a status of "Completed" (you can ignore them), and one will be running as the NGINX controller. Additionally, a NodePort service will be created. Access this service using the Node IP and the assigned NodePort. Finally, create an ingress resource using the YAML file provided in this repository

change the path, service name, namespace and ingress name as you want. then apply

```
kubectl apply -f claudie-backend-srv.yaml
```
## Then check the ingress 
```
kubectl get ingress -n claudie-backend 
```
## If there is no class then apply the class.yaml file
```
kubectl apply -f class.yaml
```
