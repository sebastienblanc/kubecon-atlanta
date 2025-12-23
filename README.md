# kubecon-atlanta

This repository contains Kubernetes manifests for demonstration purposes, including Custom Resource Definitions (CRDs), Custom Resources, and standard Kubernetes resources.

## kubectl Examples

### Applying Custom Resource Definitions (CRDs)

First, apply the Custom Resource Definitions to define new resource types:

```bash
# Apply the Prompt CRD (includes example Prompt resource)
kubectl apply -f prompt_crd_cr.yml

# Apply WebApplication CRD with standard validation
kubectl apply -f validation-example.yml

# Apply WebApplication CRD with CEL validation (simplified)
kubectl apply -f validation-example-cel.yml
```

### Applying Custom Resources

Once the CRDs are installed, you can apply the custom Prompt resources:

```bash
# Apply all Prompt resources in the manifests directory
kubectl apply -f manifests/

# Or apply individual Prompt resources
kubectl apply -f manifests/"my-cool-prompt".yaml
kubectl apply -f manifests/"my-live-demo".yaml
kubectl apply -f manifests/"prompt-4".yaml
```

### Applying Standard Kubernetes Resources

Apply the stress testing deployment:

```bash
# Apply the stress demo deployment
kubectl apply -f manifests/stress-demo.yaml
```

### Useful kubectl Commands

```bash
# List all custom resources
kubectl get prompts
kubectl get webapplications

# Describe a specific Prompt resource
kubectl describe prompt my-cool-prompt

# Get all resources in the current namespace
kubectl get all

# Check the status of the stress demo deployment
kubectl get deployment stress-demo
kubectl get pods -l app=stress-demo

# Delete resources (in reverse order)
kubectl delete -f manifests/
kubectl delete -f prompt_crd_cr.yml
kubectl delete -f validation-example.yml
kubectl delete -f validation-example-cel.yml
```
