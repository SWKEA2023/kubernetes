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
```` bash
    $ minikube start
````

`Show minikube UI interface`
```` bash
    $ minikube dashboard
````

`Show minikube UI interface`
```` bash
    $ minikube dashboard
````

`Run kubernetes clusters`
```` bash
    $ npm run up
````

`Teardown kubernetes clusters`
```` bash
    $ npm run down
````
### Without node package manager (npm)
`Run kubernetes clusters`
```` bash
    $ kubectl apply -f k8s-setup/
````

`Teardown kubernetes clusters`
```` bash
    $ kubectl delete -f k8s-setup/
````

### To serve the containers

`Open connections to all services with an ip and port`
```` bash
    $ minikube service --all
````