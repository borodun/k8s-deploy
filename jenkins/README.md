# Usage

```shell
$ helm repo add jenkins https://charts.jenkins.io
$ helm repo update
$ helm show value jenkins/jenkins > values.yaml
```

Change _values.yaml_ according to your needs and deploy Jenkins

```shell
$ helm upgrade --install jenkins jenkins/jenkins -n jenkins --create-namespace -f values.yaml
```

Change _jenkins-route.yaml_ according to your needs

```shell
$ kubectl apply -f jenkins-route.yaml
```

Add PV for Jenkins 

```shell
$ kubectl apply -f jenkins-pv.yaml
```