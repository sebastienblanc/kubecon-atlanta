# kubecon-atlanta

Kubernetes Custom Resource Definitions (CRDs) and examples for AI Prompt management.

## Prompt CRD Examples

This repository contains comprehensive examples of Prompt Custom Resources for managing AI prompts in Kubernetes environments.

### Core Prompt CRD Definition

- **`prompt_crd_cr.yml`** - Contains the Prompt CRD definition and a basic code review prompt example

### Comprehensive Prompt Examples

#### Development & Engineering Prompts
- **`prompt_cr_code_review.yml`** - Code review assistance with AI
- **`prompt_test_generator.yml`** - Generate comprehensive test cases for software components
- **`prompt_api_design_reviewer.yml`** - Review and provide recommendations for API design
- **`prompt_architecture_design.yml`** - Design and review software architecture for complex systems
- **`prompt_documentation_generator.yml`** - Generate technical documentation from code or specifications

#### Operations & Infrastructure Prompts  
- **`prompt_deployment_troubleshooter.yml`** - Troubleshoot Kubernetes deployment issues
- **`prompt_incident_response.yml`** - Guide incident response and post-mortem analysis
- **`prompt_performance_optimization.yml`** - Analyze and provide performance optimization recommendations
- **`prompt_security_analysis.yml`** - Perform security analysis on code, configurations, or infrastructure

#### Business & Analytics Prompts
- **`manifests/"my-cool-prompt".yaml`** - Customer support assistant for ticket resolution
- **`manifests/"my-live-demo".yaml`** - Interactive assistant for live demonstrations
- **`manifests/"prompt-4".yaml`** - Data analysis with insights and visualizations

### Prompt CRD Features

The Prompt CRD supports:

- **Templated prompts** with variable substitution using `{{variable_name}}` syntax
- **Argument definitions** with required/optional parameters and descriptions
- **Status tracking** (stable, experimental, deprecated)
- **Team ownership** for organizational management
- **Structured metadata** for discoverability and management

### Usage Example

```yaml
apiVersion: mcp.io/v1
kind: Prompt
metadata:
  name: my-prompt
  namespace: default
spec:
  description: "Description of what this prompt does"
  status: stable
  owner: my_team
  template: |
    You are helping with {{task_type}}.
    
    Context: {{context}}
    
    Please provide detailed assistance.
  arguments:
    - name: task_type
      description: The type of task to help with
      required: true
    - name: context
      description: Additional context for the task
      required: false
```

### Deployment

Deploy the CRD and examples:

```bash
# Install the Prompt CRD
kubectl apply -f prompt_crd_cr.yml

# Deploy individual prompt examples
kubectl apply -f prompt_documentation_generator.yml
kubectl apply -f prompt_test_generator.yml
kubectl apply -f manifests/

# List all prompt resources
kubectl get prompts
```

### Custom Resource Management

View prompt details:
```bash
kubectl describe prompt documentation-generator-prompt
```

Update done 
