# Custom Resources

This directory contains Kubernetes Custom Resource Definitions (CRDs) and example Custom Resources for the KubeCon Atlanta project.

## Quick Start

```bash
# Install all CRDs
kubectl apply -f crds/

# Create example resources
kubectl apply -f examples/
```

## Contents

- **`crds/`** - Custom Resource Definitions
- **`examples/`** - Example Custom Resource instances organized by type
- **`docs/`** - Detailed documentation and usage guides

For detailed information, see [docs/README.md](docs/README.md).

## Resource Types

- **Prompt** (`prompts.mcp.io`) - AI prompt templates
- **WebApplication** (`webapplications.platform.company.com`) - Web application configurations

## Validation

All CRDs include OpenAPI schema validation. The WebApplication CRD also includes CEL validation for production requirements.