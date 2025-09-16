# Custom Resources Organization

This folder contains Kubernetes Custom Resource Definitions (CRDs) and example Custom Resources (CRs) organized for easy discovery and management.

## Folder Structure

```
custom-resources/
├── crds/                                      # Custom Resource Definitions
│   ├── prompt-crd.yaml                        # CRD for Prompt resources
│   ├── webapplication-crd.yaml                # CRD for WebApplication resources
│   └── webapplication-crd-with-cel-validation.yaml # WebApplication CRD with CEL validation
├── examples/                                  # Example Custom Resource instances
│   ├── prompts/                               # Prompt CR examples
│   │   ├── code-review-prompt.yaml            # Code review prompt template
│   │   ├── documentation-prompt.yaml          # Documentation generation prompt
│   │   └── testing-prompt.yaml                # Test generation prompt
│   └── webapplications/                       # WebApplication CR examples
│       ├── dev-app-example.yaml               # Development environment application
│       └── prod-app-example.yaml              # Production environment application
└── docs/                                      # Documentation
    └── README.md                               # This file
```

## Custom Resource Definitions (CRDs)

### Prompt CRD (`prompts.mcp.io`)
- **Purpose**: Defines AI prompt templates for various use cases
- **Group**: `mcp.io`
- **Kind**: `Prompt`
- **Features**: 
  - Template-based prompts with parameter substitution
  - Status tracking (stable, experimental, deprecated)
  - Owner tracking for team responsibility
  - Argument definitions with validation

### WebApplication CRD (`webapplications.platform.company.com`)
- **Purpose**: Defines web applications with database and cache dependencies
- **Group**: `platform.company.com`
- **Kind**: `WebApplication`
- **Features**:
  - Environment-specific configurations (dev, staging, prod)
  - Resource selectors for databases and caches
  - Replica count management
  - Status tracking and conditions
  - CEL validation for production requirements

## Usage Examples

### Applying CRDs
```bash
# Install all CRDs
kubectl apply -f custom-resources/crds/

# Install specific CRD
kubectl apply -f custom-resources/crds/prompt-crd.yaml
```

### Creating Custom Resources
```bash
# Create prompt examples
kubectl apply -f custom-resources/examples/prompts/

# Create WebApplication examples
kubectl apply -f custom-resources/examples/webapplications/
```

### Viewing Resources
```bash
# List all prompts
kubectl get prompts

# List all webapplications
kubectl get webapplications

# Get detailed information
kubectl describe prompt code-review-prompt
kubectl describe webapplication example-prod-app
```

## Best Practices

1. **CRD Organization**: Keep CRDs in the `crds/` folder with descriptive names
2. **Example Organization**: Group examples by resource type in subfolders
3. **Naming Convention**: Use kebab-case for file names and resource names
4. **Documentation**: Each CRD should have corresponding example resources
5. **Validation**: Include OpenAPI schema validation in CRDs
6. **Status Tracking**: Implement status subresources for operational visibility

## Contributing

When adding new custom resources:

1. Place CRDs in `custom-resources/crds/`
2. Add example instances in appropriate `custom-resources/examples/` subfolders
3. Update this README to document the new resources
4. Include proper validation and status fields in CRDs
5. Follow Kubernetes naming conventions and best practices