# Kubernetes Manifests

Kubernetes configuration to deploy and scale a containerised app.

## What's included
- **deployment.yaml:** 3 replicas, resource limits, readiness and liveness probes
- **service.yaml:** exposes the app inside the cluster
- **hpa.yaml:** scales pods automatically between 2 and 6 based on CPU usage

## Tools used
Kubernetes, kubectl, minikube (or kind)

## How to use
    minikube start
    kubectl apply -f .
    kubectl get pods
    kubectl port-forward service/demo-app 8080:80

Open http://localhost:8080

## What I learned
- How Deployments, Services, and autoscaling work together
- Why health probes and resource limits matter
