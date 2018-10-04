
#create NS
    kubectl create ns hello-world
    or
    kubectl create -f namespace-hello.yaml

#deploy the pod
    kubectl create -f hello-gcp.yaml

#create the service
    kubectl create -f hello-svc-clusterip.yaml

#DNS setup
check DNS Entries, mine is hello-world-ingress-controller.xbe-euw1-sb1.adeo.cloud, so I create a DNS record with the IP of the Ingress Controller:
    kubectl get svc -n nginx-ingress

#create the ingress with certificate
    kubectl create -f hello-ingress-controler-https.yml