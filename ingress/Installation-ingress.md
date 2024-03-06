Installation of nginx ingress controller on kubernetes cluster:
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.0/deploy/static/provider/cloud/deploy.yaml
The above step will ensure to deploy nginx ingress control on your kubernetes cluster.

It creates all different required resources in ingress-nginx namespace.

Deployment of application , 
kubectl apply of deployment-v1.yml and deployment-v2.yml two different paths with two different versions of a product.

