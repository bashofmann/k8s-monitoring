# Install prometheus-operator

```
kubectl create namespace monitoring || true
kubectl apply -f basic-auth.yaml
helm upgrade --install --namespace monitoring -f values.yaml prom stable/prometheus-operator --version 8.16.0
```
