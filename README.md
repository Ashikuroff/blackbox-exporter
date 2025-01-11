# Kubernetes Monitoring Stack with Kind and GitHub Actions

This repository deploys a local Kubernetes cluster using Kind and installs the Kube Prometheus Stack and Blackbox Exporter using Helm.

## Prerequisites

- GitHub account
- Basic knowledge of Kubernetes, Helm, and GitHub Actions

## Repository Structure

- `.github/workflows/deploy.yml`: GitHub Actions workflow for deployment.
- `kind-config.yaml`: Kind cluster configuration.
- `helm/blackbox-values.yaml`: Custom values for Blackbox Exporter.
- `helm/prometheus-values.yaml`: Custom values for Kube Prometheus Stack.

## How It Works

1. The GitHub Actions workflow sets up a Kind cluster.
2. It installs the Kube Prometheus Stack and Blackbox Exporter using Helm.
3. The services are accessible on the local machine via port-forwarding.

## Accessing Services

- **Prometheus UI**: `http://localhost:9090`
- **Blackbox Exporter UI**: `http://localhost:9115`
- **Grafana UI**: `http://localhost:30002` (Username: `admin`, Password: `admin`)
