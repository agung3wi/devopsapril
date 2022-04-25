### Install Cert Manager
```
helm repo add jetstack https://charts.jetstack.io
helm repo update
helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --set installCRDs=true
```

### Install ingress nginx
```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm update
helm install ingress-controller ingress-nginx/ingress-nginx
```


## apply staging and production issuer
```
kubectl apply -f staging.yml
```

```
kubectl apply -f prod.yml
```

## sample ingress ssl
```
kubectl apply -f sample_ingress_ssl.yml
```