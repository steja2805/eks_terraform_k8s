# EKS Terraform and Kubernetes Deployment

This repository contains Terraform files for provisioning an Amazon Elastic Kubernetes Service (EKS) cluster and Kubernetes deployment files for deploying two React applications, `quizz_app` and `weather_app`. The infrastructure is defined using Terraform, and the applications are deployed to the EKS cluster using Kubernetes manifests.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Terraform Setup](#terraform-setup)
- [Kubernetes Deployment](#kubernetes-deployment)
- [Accessing Applications](#accessing-applications)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- AWS account.
- AWS IAM role with admin access.
- Terraform installed on your local machine.
- Docker installed on your local machine.
- kubectl (Kubernetes CLI) installed on your local machine.
- AWSCLI installed on your local machine.
- Docker images for the `quizz_app` and `weather_app` applications pushed to a container registry.

## Terraform Setup

you can install the terraform from the following link
[Visit official site](https://github.com]https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

## Docker Installation
```bash
sudo apt update
sudo apt install docker.io
```

## Kubectl configuratio

you can install kubectl from the official website link given below, based on your system configurations
[Visit official site](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

## AWSCLI

```bash
sudo apt update
sudo apt install python3-pip
```

```pip3 install awscli --upgrade --user```
```aws --version```
```aws configure```

##EKS creation using terraform 
clone the github repo and run ```terraform plan``` followed by `terraform apply`
Now the cluster is created.

##Creating  Pods and Deployments
run ```kubectl apply -f path_to_deployment_file```

now the environment is set up and the applications will be live.
