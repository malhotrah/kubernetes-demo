# Basic Commands

### list the pods in the kubernetes cluster
    kubectl get pods
### Detailed description of the pods curretnly running on the cluster
    kubectl get pods -o wide
### list the services in the kubernetes cluster
    kubectl get services
### list the deployments in the kubernetes cluster
    kubectl get deployments        


## Docker hub secret setup

    kubectl create secret docker-registry dockerhubcred --docker-server=https://registry.hub.docker.com --docker-username=[DOCKER-USERNAME] --docker-password=[DOCKER-PASSWORD] --docker-email=[DOCKER-EMAIL-ID]
    kubectl get secret dockerhubcred --output=yaml
    kubectl get secret dockerhubcred --output="jsonpath={.data.\.dockerconfigjson}" | base64 --decode

## GLCOUD Commands


    gcloud config set project [PROJECT-ID]
    gcloud config set compute/zone us-central1-c
    gcloud container clusters get-credentials [CLUSTER-NAME]
