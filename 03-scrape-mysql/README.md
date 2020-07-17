# MySQL

* Install the press labs mysql operator

```sh
helm repo add presslabs https://presslabs.github.io/charts
kubectl create namespace mysql-operator
helm upgrade --install mysql-operator presslabs/mysql-operator --namespace mysql-operator -f operator-values.yaml
```

* Create a secret with credentials

```sh
kubectl apply -f mysql-operator/mysql-secret.yaml
```

* Create a cluster

```sh
kubectl apply -f mysql-operator/mysql-cluster.yaml
```

* Create rules

```sh
kubectl apply -f rules/
```
