# Service Mesh

## Install istio

```
istioctl install --set profile=demo
```
## Install shop

```
kubectl create namespace shop || true
kubectl label namespace shop istio-injection=enabled || true
kubectl apply -n shop -f .
```

## Open dashobards

```
istioctl dashboard kiali
istioctl dashboard jaeger
```