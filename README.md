- Kubernetes Deployment: https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
- Kubernetes Service: https://kubernetes.io/docs/concepts/services-networking/service/
- Traefik helm chart install: https://doc.traefik.io/traefik/getting-started/install-traefik/#use-the-helm-chart
- Traefik Kubernetes Ingress: https://doc.traefik.io/traefik/providers/kubernetes-ingress/
- Traefik Kubernetes Ingress configuration: https://doc.traefik.io/traefik/providers/overview/

## STEPS

kubectl create ns testtraefik

helm install traefik traefik/traefik --values=traefik.values.yml --namespace=testtraefik

kubectl apply -f whoami-depl.yaml

kubectl apply -f ingress.yaml
