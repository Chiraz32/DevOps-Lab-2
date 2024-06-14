## DevOps Mini-Project

This repository contains a complete DevOps setup for deploying a Node.js application using Docker, Jenkins, Kubernetes, and Ansible.

### Repository Contents

#### Dockerfile
Creates a Docker image for the Node.js app.
- **Key Steps**:
  - Set up working directory
  - Copy `package.json`
  - Install dependencies
  - Copy app files
  - Expose port 80
  - Run `server.js`

#### Jenkinsfile
Defines a Jenkins pipeline for CI/CD.
- **Stages**:
  1. **Pull from GitHub**: Clone the repository.
  2. **Build Docker Image**: Build and tag the Docker image.
  3. **Login to Docker Hub**: Authenticate with Docker Hub.
  4. **Push to DockerHub**: Push the Docker image.

#### Kubernetes Deployment
Deploys the Node.js app on a Kubernetes cluster.
- **Key Details**:
  - Run 2 replicas
  - Use image `chirazdoss/mon-app:v1`
  - Expose port 80

#### Ansible Playbook
Deploys the Node.js app on Azure servers.
- **Tasks**:
  - Install Node.js and npm
  - Clone the app from GitHub
  - Install dependencies
  - Start the app

#### Inventory File
Defines target servers for Ansible.
- **Details**:
  - Lists Azure server with IP, SSH user, and private key.

### Summary
This repository automates building, deploying, and managing a Node.js application using Docker, Jenkins, Kubernetes, and Ansible.

