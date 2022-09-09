# Usage

[Docs](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack)

```shell
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm show values prometheus-community/kube-prometheus-stack > values.yaml
```

Change _values.yaml_ according to your needs and deploy. It will install some useful CRDs and Grafana with default
dashboards

```shell
helm upgrade --install prometheus prometheus-community/prometheus -n monitoring --create-namespace -f values.yaml
```

To monitor your application
see [scrape guide](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack#prometheusioscrape)
\

To access Grafana create Traefik route:

```shell
kubectl apply -f grafana-route.yaml
```

Password for Grafana _admin_ user is in _prometheus-grafana_ secret.