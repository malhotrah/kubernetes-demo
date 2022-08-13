# Basic Commands


## Docker hub secret setup


    kubectl create secret docker-registry dockerhubcred --docker-server=https://registry.hub.docker.com --docker-username=[DOCKER-USERNAME] --docker-password=[DOCKER-PASSWORD] --docker-email=[DOCKER-EMAIL-ID]
    kubectl get secret dockerhubcred --output=yaml
    kubectl get secret dockerhubcred --output="jsonpath={.data.\.dockerconfigjson}" | base64 --decode



## GLCOUD Commands


    gcloud config set project [PROJECT-ID]
    gcloud config set compute/zone us-central1-c
    gcloud container clusters get-credentials [CLUSTER-NAME]
