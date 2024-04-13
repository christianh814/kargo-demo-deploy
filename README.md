# kargo-demo-deploy


Deployment Repo for Kargo Demo App:

After setting up Kargo (with your secret to your git repo), run:

(Assumes you've logged in with `kargo login`)

```
kubectl apply -f kargo/kargo-ing.yaml
kargo create project kargo-demo
kargo create credentials \
--project=kargo-demo kargo-demo-repo \
--git --repo-url=https://github.com/christianh814/kargo-demo-deploy \
--username=christianh814 --password=${KARGO_GH_PAT}
kubectl apply -k ./deploy
```
