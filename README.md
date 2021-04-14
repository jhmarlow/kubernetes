# Kubernetes
Repository containing files to work with k8s.

Tools:
- Minikube
- Helm

## Minikube

To install 
https://minikube.sigs.k8s.io/docs/start/

Start local cluster:

`minikube start`

Stop local cluster:

`minikube stop`

Delete clusters:

`minikube delete --all`

Deploying docker image to minikube:
https://dzone.com/articles/running-local-docker-images-in-kubernetes-1

exposing external IPs with load balancer on minikube
`minikube tunnel`
App available at: http://127.0.0.1:8000


# Helm 

`helm install <name> <path to chart>`

`helm delete <name>`

## Deploy Airflow
https://docs.bitnami.com/tutorials/deploy-apache-airflow-kubernetes-helm/

`helm install airflowrelease bitnami/airflow --set airflow.cloneDagFilesFromGit.enabled=true,airflow.cloneDagFilesFromGit.repository=https://github.com/jhmarlow/apache-airflow.git,airflow.cloneDagFilesFromGit.branch=master,airflow.baseUrl=http://127.0.0.1:8080`

`echo URL  : http://127.0.0.1:8080`
`kubectl port-forward --namespace default svc/airflowrelease 8080:8080`

`minikube tunnel`

## Google Kubernetes Engine (GKE)
Spin up a cluster using Terraform from [Terraform Github repository](https://github.com/jhmarlow/terraform.git).

## Repository
### Sockshop
Manifests from Jetstack examples.

