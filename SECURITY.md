# Security Policy

## Reporting Security Vulnerabilities

We take the security of this project seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### How to Report a Security Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them via one of the following methods:

1. **GitHub Security Advisories**: Use the "Report a vulnerability" button in the [Security tab](https://github.com/sebastienblanc/kubecon-atlanta/security) of this repository
2. **Email**: Send an email to the repository maintainer with details of the vulnerability

Please include the following information in your report:

- Description of the vulnerability
- Steps to reproduce the issue
- Potential impact of the vulnerability
- Any suggested fixes or mitigation strategies

### What to Expect

After you submit a vulnerability report, you can expect:

- **Acknowledgment**: We will acknowledge receipt of your vulnerability report within 48 hours
- **Investigation**: We will investigate and validate the reported vulnerability
- **Communication**: We will keep you informed of our progress throughout the process
- **Resolution**: We will work to address confirmed vulnerabilities in a timely manner

## Supported Versions

This project is currently in active development. Security updates will be applied to the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |

## Security Best Practices

When using this project, please consider the following security best practices:

### Kubernetes Security

- Ensure your Kubernetes cluster follows security best practices
- Use RBAC (Role-Based Access Control) to limit permissions
- Regularly update your Kubernetes cluster and nodes
- Implement network policies to restrict pod-to-pod communication
- Use secure image registries and scan container images for vulnerabilities

### Custom Resource Definitions (CRDs)

- Validate input data through OpenAPI schemas defined in CRDs
- Implement proper RBAC rules for custom resources
- Regularly review and audit custom resource permissions
- Use validation webhooks for additional security checks

### General Security

- Keep all dependencies up to date
- Use the principle of least privilege
- Regularly audit and review access permissions
- Monitor your deployments for unusual activity

## Security Resources

- [Kubernetes Security Best Practices](https://kubernetes.io/docs/concepts/security/)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

## Disclaimer

This security policy applies to the code and configurations provided in this repository. Users are responsible for ensuring the security of their own deployments and infrastructure.