## Installation of NGINX Ingress Controller on Kubernetes Cluster

To install the NGINX Ingress Controller on your Kubernetes cluster, follow these steps:

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.0/deploy/static/provider/cloud/deploy.yaml

It creates all different required resources in ingress-nginx namespace.

Deployment of application , 
kubectl apply of deployment-v1.yml and deployment-v2.yml two different paths with two different versions of a product.

