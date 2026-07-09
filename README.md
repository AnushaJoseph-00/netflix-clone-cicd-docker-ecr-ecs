# Netflix Clone CI/CD Pipeline — Jenkins, SonarQube, Docker, ECR and ECS
A containerized CI/CD pipeline for a Netflix clone application, built with Jenkins, SonarQube, Docker, Amazon ECR, and AWS ECS (Fargate). This project is an extension of my earlier native-install CI/CD pipeline, rebuilt to demonstrate containerization and cloud-native deployment.

## Overview

The previous CI/CD project used Jenkins, SonarQube, and Nexus on EC2, with the app served directly by an nginx server. This version keeps Jenkins and SonarQube as native installs for build orchestration and code quality analysis, but replaces the nginx deployment layer entirely with Docker, AWS ECR, and AWS ECS:

- The application is containerized with **Docker**
- Images are pushed to **Amazon ECR**
- The container is deployed and run via **AWS ECS (Fargate)**, behind an **Application Load Balancer**

## Architecture
