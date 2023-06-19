# Project Name

This is sample asp.net core web api using .net 6.0 and it is using mongo db for database.You can create a docker image and push to docker hub.Using docker hub image, you can install that image in any kuberentes clusters.

## Table of Contents

- [Project Description](#project-description)
- [Repository Link](#repository-link)
- [Docker Hub](#docker-hub)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoint](#api-endpoint)
- [Kubernetes Deployment](#kubernetes-deployment)
- [Contributing](#contributing)
- [License](#license)

## Project Description

This is an ASP.NET Core Web API project that utilizes MongoDB as the database and is hosted on Google Cloud Platform (GCP) Kubernetes Cluster.

## Repository Link

The code for this project can be found on [GitHub](https://github.com/ArunVashishtha/MicroService_MongoDB_K8).

## Docker Hub

Docker images for this project are hosted on [Docker Hub](https://hub.docker.com/r/arunvashishtha/microservicewithmongo).

To pull the Docker image, use the following command:

    docker pull arunvashishtha/microservicewithmongo

## Installation
You can download the code for given repository and after dowloading build the project and run locally or globally using docker hub image.

## Build an image
Download the source code, and build your image using below steps:

Build the Docker image: Open a terminal or command prompt, navigate to the directory containing the Dockerfile, and run the following command:

    docker build -t your-dockerhub-username/your-image-name:tag .

Replace your-dockerhub-username, your-image-name, and tag with appropriate values. The . at the end specifies the build context as the current directory.
Log in to Docker Hub: Run the following command and provide your Docker Hub credentials when prompted:

    docker login

Tag the Docker image: After a successful build, tag the image with your Docker Hub repository name:

    docker tag your-dockerhub-username/your-image-name:tag your-dockerhub-username/your-image-name:tag

Replace your-dockerhub-username, your-image-name, and tag with appropriate values.

    Push the Docker image to Docker Hub: Run the following command to push the tagged image to Docker Hub:
    
    docker push your-dockerhub-username/your-image-name:tag

Replace your-dockerhub-username, your-image-name, and tag with appropriate values.

## API Endpoint
The service API tier can be accessed at the following URL to view the records from the backend tier:

    http://34.170.168.250/items

## Kubernetes Deployment
To deploy the pods for the above image in Kubernetes, execute the following commands:

- Create the MongoDB secrets:

    kubectl apply -f mongodb-secrets.yaml

- Create the MongoDB ConfigMap:

    kubectl apply -f mongodb-configmap.yaml

- Create the MongoDB deployment:

  kubectl apply -f mongodb-deployment.yaml

  Before applying the below command, please check the image name in the catalog-deployment.yaml file it should same as it is given in the repository or your can update image name in this file as per your image and tag.

- Create the catalog deployment:

    kubectl apply -f catalog-deployment.yaml

Make sure to update the file names to match your actual YAML files.

License
Specify the license under which the project is distributed.




