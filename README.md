# k8s-lab-bootstrap

```
helm repo add k8s-lab-bootstrap https://wiktorvip.github.io/k8s-lab-bootstrap
helm repo update
helm search repo k8s-lab-bootstrap --versions
helm install metallb-umbrella k8s-lab-bootstrap/metallb-config --create-namespace --namespace metallb-system
```
