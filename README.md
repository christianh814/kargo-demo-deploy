# kargo-demo-deploy

Deployment Repo for Kargo Demo App:

After setting up Kargo (with your secret to your git repo), run:

```
kubectl create ns kargo-demo
kubectl apply -f /path/to/kargo/kargo-repo-secret.yaml
kubectl apply -k ./deploy
```
