# ArgoCD

Use the official manifest file to deploy ArgoCD to a Kubernetes cluster:
[ArgoCD Install Manifest](https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml)

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

To Convert the ArgoCD service from ClusterIP to NodePort to allow external browser access.

```
kubectl patch svc argocd-server -n default -p '{"spec":{"type":"NodePort"}}'
```
