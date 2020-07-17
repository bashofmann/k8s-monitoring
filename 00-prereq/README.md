# Prerequisites

## Install Longhorn

## Install cert-manager

```
kubectl create namespace cert-manager || true
helm upgrade --install cert-manager jetstack/cert-manager --namespace cert-manager --version v0.15.2 --set installCRDs=true --wait
kubectl apply -f cluster-issuer.yaml
kubectl apply -f cluster-issuer-credentials.yaml
```

## Install external-dns

```
kubectl create namespace external-dns || true
helm upgrade --install external-dns bitnami/external-dns --namespace=external-dns --version 2.20.4 -f external-dns-values.yaml
```