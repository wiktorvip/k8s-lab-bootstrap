# k8s-lab-bootstrap
### labA
```
Get password of argocd admin user:
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

argocd login 172.16.200.20:30888
argocd proj list
argocd app list


Infra 1
k apply -f https://raw.githubusercontent.com/wiktorvip/labA/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject1.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/labA/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra1.yaml

Infra 2
k apply -f https://raw.githubusercontent.com/wiktorvip/labA/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject2.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/labA/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra2.yaml


### labB

```
Get password of argocd admin user:
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

argocd login 10.0.0.110:30888
argocd proj list
argocd app list


Infra 1
k apply -f https://raw.githubusercontent.com/wiktorvip/labB/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject1.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/labB/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra1.yaml

Infra 2
k apply -f https://raw.githubusercontent.com/wiktorvip/labB/k8s-lab-bootstrap/refs/heads/main/argocd/AppProject2.yaml
k apply -f https://raw.githubusercontent.com/wiktorvip/labB/k8s-lab-bootstrap/refs/heads/main/argocd/App-infra2.yaml


```

```
helm repo add k8s-lab-bootstrap https://wiktorvip.github.io/k8s-lab-bootstrap
helm repo update
helm search repo k8s-lab-bootstrap --versions
helm install metallb-umbrella k8s-lab-bootstrap/metallb-config --create-namespace --namespace metallb-system
```
