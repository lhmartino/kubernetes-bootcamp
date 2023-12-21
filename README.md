## Set Up the Node demo Application

## Build and push a Docker Image

    docker build -t node-image .

    docker image tag node-image <username>/node-image

    docker push <username>/node-image

You can test your dockerfile running:

    docker run -dp 8000:8000 <username>/node-image



## Using/installing kubectl / minikube

### Install Kubectl
https://kubernetes.io/docs/tasks/tools/#kubectl

Test kubectl installation using:
    
    kubectl version --client

### Install minukube
https://minikube.sigs.k8s.io/docs/start/

Test minikube installation using:

    minikube version

Run minikube using:

    minikube start 

## Create the Pod, Deployment, and Service    

At the k8s directory, run:

    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml

Check your pods, deployments, and services using the kubectl get [pods, deployments, svc]

To check logs, use:

    kubectl logs [resource-name]

### Using minikube dashboard

Just run:

    minikube dashboard

### Access Your Application

To discover the service endpoint, run:

    minikube service <service-name> --url

## Scaling Your Application

To scale up your application, increase the number of replicas of your deployment by running the following command:

    kubectl scale deployment <deployment-name> --replicas=<desired-number>


