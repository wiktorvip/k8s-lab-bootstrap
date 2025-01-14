# k8s-lab-bootstrap

```

Infra 1
k apply -f https://raw.githubusercontent.com/wiktorvip/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject1.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra1.yaml

Infra 2
k apply -f https://raw.githubusercontent.com/wiktorvip/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject2.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra2.yaml


```

```
helm repo add k8s-lab-bootstrap https://wiktorvip.github.io/k8s-lab-bootstrap
helm repo update
helm search repo k8s-lab-bootstrap --versions
helm install metallb-umbrella k8s-lab-bootstrap/metallb-config --create-namespace --namespace metallb-system
```
