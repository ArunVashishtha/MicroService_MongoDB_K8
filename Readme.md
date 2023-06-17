# Project Name

Project description goes here.

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

The code for this project can be found on [GitHub](https://www.github.com).

## Docker Hub

Docker images for this project are hosted on [Docker Hub](https://hub.docker.com/r/arunvashishtha/microservicewithmongo).

To pull the Docker image, use the following command:

docker pull arunvashishtha/microservicewithmongo

Installation
You can download the code for given repository and after dowloading build the project and run locally or globally using docker hub image.

API Endpoint
The service API tier can be accessed at the following URL to view the records from the backend tier:

http://34.170.168.250/items

Kubernetes Deployment
To deploy the pods for the above image in Kubernetes, execute the following commands:

Create the MongoDB secrets:
kubectl apply -f mongodb-secrets.yaml

Create the MongoDB ConfigMap:
kubectl apply -f mongodb-configmap.yaml

Create the MongoDB deployment:
kubectl apply -f mongodb-deployment.yaml

Create the catalog deployment:
kubectl apply -f catalog-deployment.yaml

Make sure to update the file names to match your actual YAML files.

License
Specify the license under which the project is distributed.




