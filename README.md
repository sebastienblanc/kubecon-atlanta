# KubeCon Atlanta

This repository contains Kubernetes manifests and Custom Resource Definitions for the KubeCon Atlanta demonstration.

## Prerequisites

To run this project, you need a Kubernetes cluster. The easiest way to get one running locally is to install **minikube** on your laptop.

## Installing minikube

minikube is a tool that lets you run Kubernetes locally. It creates a single-node Kubernetes cluster inside a virtual machine on your laptop.

### System Requirements

- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection
- Container or virtual machine manager, such as: Docker, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox, or VMware

### Installation Instructions

#### macOS

**Option 1: Using Homebrew (Recommended)**
```bash
brew install minikube
```

**Option 2: Using curl**
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
```

For Apple Silicon Macs (M1/M2):
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64
sudo install minikube-darwin-arm64 /usr/local/bin/minikube
```

#### Linux

**Option 1: Using curl (x86-64)**
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

**Option 2: Using package managers**

For Debian/Ubuntu:
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
```

For Red Hat/CentOS/Fedora:
```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-latest.x86_64.rpm
sudo rpm -Uvh minikube-latest.x86_64.rpm
```

#### Windows

**Option 1: Using Chocolatey**
```powershell
choco install minikube
```

**Option 2: Using Windows Package Manager**
```powershell
winget install minikube
```

**Option 3: Direct download**
Download the latest release from the [minikube releases page](https://github.com/kubernetes/minikube/releases) and add it to your PATH.

### Starting minikube

Once installed, start your minikube cluster:

```bash
minikube start
```

This command will:
- Download the Kubernetes ISO
- Create a virtual machine
- Configure kubectl to use the minikube cluster

### Verify Installation

Check that minikube is running:
```bash
minikube status
```

Check that kubectl can connect to your cluster:
```bash
kubectl cluster-info
```

### Useful minikube Commands

```bash
# Start minikube
minikube start

# Stop minikube
minikube stop

# Delete minikube cluster
minikube delete

# Open Kubernetes dashboard
minikube dashboard

# Get minikube IP
minikube ip

# SSH into minikube
minikube ssh

# Check minikube status
minikube status
```

## Running the Project

Once you have minikube running, you can deploy the manifests in this repository:

```bash
# Apply all manifests
kubectl apply -f manifests/

# Apply specific validation examples
kubectl apply -f validation-example.yml
kubectl apply -f validation-example-cel.yml

# Apply custom resource definitions
kubectl apply -f prompt_crd_cr.yml
```

## Troubleshooting

If you encounter issues:

1. **Check minikube status**: `minikube status`
2. **View minikube logs**: `minikube logs`
3. **Restart minikube**: `minikube stop && minikube start`
4. **Check available resources**: `minikube addons list`

For more detailed troubleshooting, visit the [minikube documentation](https://minikube.sigs.k8s.io/docs/).

## Additional Resources

- [minikube Documentation](https://minikube.sigs.k8s.io/docs/)
- [Kubernetes Documentation](https://kubernetes.io/docs/)
- [kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)
