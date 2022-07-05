# argocd-helm-chart
Deploy ArgoCD via the official Helm chart using the dependency feature

## Dependencies
* helm3

## Install

```
helm dependency update
helm upgrade --install argocd . -n argocd -f values-override.yaml
```

should not be necessary, but to install CRDs manually:
```
kubectl -f https://github.com/argoproj/argo-helm/tree/02c655ff9a6c713f8c8b083a300558e0eb86ff1c/charts/argo-cd/crds
```
