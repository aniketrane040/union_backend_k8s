# Union Backend Application - Kubernetes Deployment

This repository contains the Kubernetes manifests to deploy the Union Backend application along with MongoDB on an EKS cluster. We use NGINX as the Ingress Controller to manage external access to the application.

## Prerequisites

- A running Kubernetes cluster (EKS or another Kubernetes provider)
- Helm installed on your local machine
- `kubectl` configured to interact with your Kubernetes cluster

## Step 1: Install NGINX Ingress Controller

The first step is to install the NGINX Ingress Controller in your Kubernetes cluster. This will manage the routing of external traffic to your application.

1. **Add the NGINX Ingress Helm repository:**

   ```bash
   helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
   helm repo update
