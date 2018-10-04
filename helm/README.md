#Get helm for mac:
    brew install kubernetes-helm

#Install Helm:

    kubectl create ns tiller
    kubectl create -f helm-sa.yaml
    helm init --tiller-namespace tiller --service-account helm