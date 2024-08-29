# Union-App Kubernetes Deployment

This repository contains Kubernetes manifests for deploying the Union-App backend with MongoDB on an EKS cluster using Istio for ingress.

## Prerequisites

- A Kubernetes cluster (EKS, GKE, Minikube, etc.)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Helm](https://helm.sh/docs/intro/install/)
- Istio installed on the cluster

## Installation

### 1. Install Istio

If Istio is not already installed, follow these steps:

```bash
helm repo add istio https://istio-release.storage.googleapis.com/charts
helm repo update

# Install Istio base CRDs
helm install istio-base istio/base -n istio-system --create-namespace

# Install Istio control plane
helm install istiod istio/istiod -n istio-system

# Install Istio ingress gateway
helm install istio-ingressgateway istio/gateway -n istio-system
```

### 2. Install Helm Release

```bash
helm install union-app-relase .
```


### 3. Access the Application

Access application on istio gateway endpoint

```bash
kubectl get svc istio-ingressgateway -n istio-system
