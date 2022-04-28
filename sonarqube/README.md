# Usage

```shell
$ helm repo add sonarqube https://SonarSource.github.io/helm-chart-sonarqube
$ helm repo update
$ helm show values sonarqube/sonarqube > values.yaml
```

Change _values.yaml_ according to your needs and deploy SonarQube. \

```shell
$ helm upgrade --install sonarqube sonarqube/sonarqube -n sonarqube --create-namespace -f values.yaml
```

Change _sonarqube-route.yaml_ according to your needs. \

```shell
$ kubectl apply -f sonarqube-route.yaml
```

Add PV for SonarQube \

```shell
$ kubectl apply -f sonarqube-pv.yaml
```