__HOW TO INSTALL NGINX INGRESS CONTROLLER__

Go to this document

https://github.com/kubernetes/ingress-nginx/blob/main/docs/deploy/index.md#bare-metal-clusters

And follow up the commands

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.1/deploy/static/provider/baremetal/deploy.yaml

it will create namespace as ingress-nginx and some pods there will be three pods 2 will be in completed state ignore them and one will be running as nginx controller
And one nodeport svc browse that port with node ip then create ingress with provided yaml in this repository

change the path and service name and namespace ingress name as you want and apply

kubectl apply -f claudie-backend-srv.yaml
