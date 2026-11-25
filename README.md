# Game 2048 Application Deployment on AWS EKS

## Project Overview

This project demonstrates the deployment of a containerized 2048 game application on **Amazon Elastic Kubernetes Service (EKS)** using Kubernetes and AWS cloud infrastructure.

The application is deployed using Kubernetes Deployments and Services, while AWS Load Balancer Controller integrates Kubernetes Ingress with an AWS Application Load Balancer (ALB) to provide external access to the application.

The project focuses on understanding container orchestration, cloud infrastructure, Kubernetes networking, IAM permissions and application deployment on AWS.

## Architecture

The project uses Amazon EKS to manage and orchestrate containerized application workloads. AWS Fargate provides serverless compute capacity for running Kubernetes Pods.

Application traffic flows through the AWS Application Load Balancer to the Kubernetes Service, which distributes requests to the application Pods.

## Project Workflow

### 1. AWS Infrastructure Setup
- Configured AWS CLI and established connectivity with AWS.
- Created an Amazon EKS cluster using eksctl.
- Configured VPC networking with public and private subnets.
- Used AWS Fargate for serverless container execution.

### 2. Kubernetes Cluster Configuration
- Connected the local Kubernetes environment to the EKS cluster.
- Configured Kubernetes access using kubectl.
- Created a dedicated namespace to organize application resources.

### 3. Application Deployment
- Deployed the containerized 2048 game application on Amazon EKS.
- Used Kubernetes Deployments to manage application Pods.
- Configured multiple replicas for application availability.
- Created Kubernetes Services to provide stable internal communication with application Pods.

### 4. IAM and OIDC Integration
- Configured an OIDC identity provider for the EKS cluster.
- Created IAM policies and roles for AWS resource permissions.
- Integrated IAM Roles for Service Accounts (IRSA) to provide secure AWS access to Kubernetes workloads.

### 5. AWS Load Balancer Controller
- Installed AWS Load Balancer Controller using Helm.
- Integrated Kubernetes Ingress with AWS Application Load Balancer.
- Enabled automated provisioning and configuration of the load balancer.

### 6. Application Exposure and Testing
- Configured Kubernetes Ingress for external application access.
- Used AWS Application Load Balancer to receive incoming HTTP traffic.
- Routed incoming requests to the Kubernetes Service and application Pods.
- Verified application accessibility through the ALB DNS endpoint.

## Technologies Used

- **Cloud Platform:** AWS
- **Containerization:** Docker
- **Container Orchestration:** Kubernetes
- **Managed Kubernetes:** Amazon EKS
- **Compute:** AWS Fargate
- **Infrastructure Networking:** Amazon VPC, Subnets
- **Identity and Access Management:** AWS IAM, OIDC, IRSA
- **Load Balancing:** AWS Application Load Balancer
- **Package Management:** Helm
- **Cluster Management:** eksctl, kubectl
- **Application:** 2048 Game

## Key Learnings

- Understanding Amazon EKS architecture and managed Kubernetes.
- Deploying containerized applications on AWS.
- Managing application workloads using Kubernetes Deployments and Services.
- Understanding Kubernetes Ingress and external traffic routing.
- Configuring AWS IAM roles and OIDC integration.
- Using Helm to install Kubernetes components.
- Integrating AWS Load Balancer Controller with Amazon EKS.
- Understanding application networking and load balancing in AWS.

## Project Outcome

Successfully deployed the 2048 game application on Amazon EKS and exposed it externally through an AWS Application Load Balancer.

This project provided practical experience with Kubernetes orchestration, AWS cloud infrastructure, serverless container execution, IAM integration and application networking.
