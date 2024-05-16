# kubernetes

This is a repo for orchestration the dls projects microservices and databases

# Tools to de installed

- Docker desktop
- Kubernetes on docker desktop: https://docs.docker.com/desktop/kubernetes/
- Minikube: https://minikube.sigs.k8s.io/docs/start/
- Kubectl:
  - Linux: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
  - macOS: https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/
  - Windows: https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/

## Driver

- docker driver

# Guide

`Start minikube`

```bash
    $ minikube start
```

`Show minikube UI interface`

```bash
    $ minikube dashboard
```

`Show minikube UI interface`

```bash
    $ minikube dashboard
```

`Run kubernetes clusters`

```bash
    $ npm run up
```

`Teardown kubernetes clusters`

```bash
    $ npm run down
```

### Without node package manager (npm)

`Run kubernetes clusters`

```bash
    $ kubectl apply -f k8s-setup/
```

`Teardown kubernetes clusters`

```bash
    $ kubectl delete -f k8s-setup/
```

### To serve the containers

`Open connections to all services with an ip and port`

```bash
    $ minikube service --all
```

# Docker compose guide

``When the containers is running, restart email, transaction and admin containers.``</br>

## Seeding the database
To seed the database go into the exec command line inside the admin container and run:</br>
```` bash
    npm run pop
````


## OpenAPI access
Run endpoints when compose is running.

``AdminAPI``</br>
http://localhost:3000/api</br>
</br>

``CinemaAPI``</br>
http://localhost:3002/api</br>


## Env

````
# Docker Configuration
STACK_VERSION=8.13.0
LICENSE=basic

# Elastic Stack Configuration
ELASTIC_PASSWORD=password1234
ES_PORT=9200
CLUSTER_NAME=docker-cluster

# Kibana Configuration
KIBANA_PASSWORD=password1234
KIBANA_PORT=5601

# Memory Configuration
ES_MEM_LIMIT=1073741824
KB_MEM_LIMIT=1073741824
LS_MEM_LIMIT=1073741824

# Sample Configuration (POC environments)
ENCRYPTION_KEY=c34d38b3a14956121ff2170e5030b471551370178f43e5626eec58b04a30fae2
````

For the mail to send, use trapmail.io and signup.</br>
After signup insert the username and password in the env values

```
    - MAIL_USERNAME=<username_from_trapmail>
    - MAIL_PASSWORD=<password_from_trapmail>
```
