# ArgoCD Applications

This directory contains ArgoCD application definitions for deploying various services and tools in a Kubernetes cluster. Each subdirectory represents a different application or service, with its own `kustomization.yaml` file for managing configurations.

## ArgoCD configuration for kustomize

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: argocd-cm
data:
  # enables a kustomization option that can work with remote helm repos
  kustomize.buildOptions: --enable-helm --load-restrictor=LoadRestrictionsNone # Add this configuration
```
