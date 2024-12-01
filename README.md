# Project Overview
This project showcases the complete workflow for building, configuring, and deploying a web application infrastructure using modern DevOps tools and practices. The solution integrates Terraform for infrastructure 

provisioning, Ansible for configuration management, Kubernetes for container orchestration, and Jenkins for Continuous Integration and Continuous Deployment (CI/CD).

Objectives
Infrastructure Setup:

Use Terraform modules to create a secure and scalable cloud infrastructure.

Build a Virtual Private Cloud (VPC) with two public subnets for hosting EC2 instances and Elastic Kubernetes Service (EKS).

Launch an EC2 instance in a public subnet with internet access.

Deploy a Kubernetes cluster using EKS within the same VPC.

# Configuration Management:

Automate the setup of Jenkins and its dependencies on the EC2 instance using Ansible playbooks for consistent configuration.
Source Code Management:

Set up a GitHub repository for a sample web application 

Create a Dockerfile to containerize the web application

Develop Kubernetes deployment and service manifests to manage the application lifecycle.

# Kubernetes Deployment:

Configure namespace in the Kubernetes cluster.

Deploy the application to the namespace using a LoadBalancer service to expose it for external access.

# CI/CD Pipeline Implementation:

Integrate Jenkins with GitHub to automate the CI/CD pipeline.

Create a Jenkins pipeline for to automate Docker image builds and application deployments.

Configure a GitHub webhook to trigger the pipeline upon code pushes, ensuring continuous updates to the Dev namespace.

# Technologies and Tools

Terraform: For automated infrastructure provisioning and management.

Ansible: To automate configuration tasks and system setup.

Kubernetes: For containerized application orchestration and scaling.

AWS EKS: Managed Kubernetes service for seamless cluster management.

Jenkins: For implementing Continuous Integration and Continuous Deployment pipelines.

Docker: To containerize the web application 
