# QANP CSI Driver for Kubernetes
This is official [Container Storage Interface](https://github.com/container-storage-interface) driver for QNAP NAS.

## Software Prerequisites
### CSI Driver version and Compatibility
| Driver Version  | Supported k8s version   | Supported QNAP NAS version |
| ----------------| ------------------------|----------------------------|
| v0.0.0-beta     |     1.14 to 1.23        | QuTS 5.0.0 or later        |

### Supported host operating systems
- Debian 8 or later
- Ubuntu 16.04 or later
- CentOS 7.0 or later
- RHEL 7.0 or later
- CoreOS 1353.8.0 or later

## Supported feature

# Deploy
## Before starting
### Additional install item in k8s environment
Master and worker node should install:
```
apt install open-iscsi
```

### Qualify your Kubernetes cluster
1.	Minikube is not supported
2.	Make sure “kubectl” works well
2.1.	kubectl get pods
2.2.	kubectl version
3.	Make sure you are Kubernetes cluster administrator
3.1.	kubectl auth can-i '*' '*' --all-namespaces
3.2.	Should be yes
