# Commands

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
kubectl port-forward svc/argocd-server -n argocd 8080:443
argocd admin initial-password -n argocd
argocd login <ARGOCD_SERVER>
argocd account update-password
kubectl get secret argocd-initial-admin-secret -n argocd -o yaml
echo <PASSWORD> | base64 --decode
```

---

# Links 

