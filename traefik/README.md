# Usage

[Docs](https://doc.traefik.io/traefik/) \
[Videos](https://www.youtube.com/playlist?list=PL34sAs7_26wNldKrBBY_uagluNKC9cCak)

```shell
helm repo add traefik https://helm.traefik.io/traefik
helm repo update
helm show traefik/traefik values > values.yaml
```

Change _values.yaml_ according to your needs and deploy Traefik

```shell
helm upgrade --install traefik traefik/traefik -n traefik --create-namespace -f values.yaml
```

Change _dashboard-route.yaml_ if you want to access Traefik dashboard (NOTE: it's not secure, add at
least [BasicAuth](https://doc.traefik.io/traefik/middlewares/http/basicauth/#basicauth) middleware)

```shell
kubectl apply -f dashboard-route.yaml
```

Add PV for certificates

```shell
kubectl apply -f traefik-pv.yaml
```