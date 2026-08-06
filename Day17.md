# Kubernetes (K8s) - Complete Notes

## Table of Contents

1. What is Kubernetes?
2. What is a Container?
3. What is Container Orchestration?
4. Kubernetes Features
5. Kubernetes Architecture
6. Kubernetes Components
7. Control Plane Components
8. Worker Node Components
9. Kubernetes Workflow
10. Important Definitions
11. Summary Table

---

# 1. What is Kubernetes?

**Kubernetes (K8s)** is an open-source **Container Orchestration Platform** used to automate the deployment, scaling, networking, and management of containerized applications across multiple machines.

### Key Functions
- Deploy applications automatically
- Scale applications
- Restart failed containers
- Load balance traffic
- Perform rolling updates
- Roll back failed deployments

---

# 2. What is a Container?

A **Container** is a lightweight, portable package that contains:

- Application
- Libraries
- Dependencies
- Runtime
- Configuration Files

Containers ensure applications run the same way on every system.

Example:

```
Docker Container
│
├── Application
├── Libraries
├── Dependencies
└── Runtime
```

---

# 3. What is Container Orchestration?

Container Orchestration is the automated management of multiple containers.

It performs:

- Deployment
- Scaling
- Load Balancing
- Monitoring
- Networking
- Self-Healing
- Rolling Updates

Kubernetes is the most popular container orchestration platform.

---

# 4. Kubernetes Features

## 1. Automated Deployment

Automatically deploys applications from YAML files.

---

## 2. Auto Scaling

Automatically increases or decreases Pods according to traffic.

---

## 3. Self-Healing

Automatically restarts failed Pods or Containers.

---

## 4. Load Balancing

Distributes incoming traffic evenly among Pods.

---

## 5. Rolling Updates

Updates applications without downtime.

---

## 6. Rollback

Restores the previous version if the new deployment fails.

---

## 7. Service Discovery

Provides a stable IP/DNS name to communicate with Pods.

---

## 8. Secret Management

Stores passwords, API keys, and certificates securely.

---

## 9. Storage Management

Uses Persistent Volumes (PV) and Persistent Volume Claims (PVC) for persistent storage.

---

# 5. Kubernetes Architecture

```
                    Kubernetes Cluster
                  _______________________

                  Control Plane (Master)
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
     Worker Node      Worker Node       Worker Node
```

A Kubernetes Cluster consists of:

- Control Plane
- Worker Nodes

---

# 6. Kubernetes Components

## Cluster

A collection of Worker Nodes managed by the Control Plane.

---

## Node

A physical or virtual machine participating in the cluster.

Types:

- Control Plane Node
- Worker Node

---

## Pod

The smallest deployable unit in Kubernetes.

A Pod contains one or more containers sharing:

- Network
- Storage
- IP Address

Example

```
Pod
│
├── Container 1
└── Container 2
```

---

## Deployment

Manages Pods and ensures the desired number of replicas are running.

Supports:

- Scaling
- Rolling Updates
- Rollbacks

---

## ReplicaSet

Ensures a fixed number of Pod replicas remain running.

Example:

Desired Pods = 3

If one Pod crashes,

ReplicaSet creates another Pod automatically.

---

## Service

Provides a stable endpoint to access Pods.

Functions:

- Load Balancing
- Stable IP
- Service Discovery

---

## Namespace

Provides logical separation of Kubernetes resources.

---

# 7. Control Plane Components

The Control Plane is the brain of Kubernetes.

Components:

```
Control Plane

├── API Server
├── Scheduler
├── Controller Manager
└── etcd
```

---

## API Server (kube-apiserver)

### Definition

The API Server is the central communication hub of Kubernetes.

Every request passes through it.

### Responsibilities

- Accepts requests
- Authenticates users
- Validates requests
- Stores data in etcd
- Communicates with all components

---

## Scheduler (kube-scheduler)

### Definition

Assigns newly created Pods to the most suitable Worker Node.

### Considers

- CPU
- RAM
- Affinity Rules
- Node Labels
- Taints & Tolerations

---

## Controller Manager (kube-controller-manager)

### Definition

Maintains the desired state of the cluster.

Example

Desired Pods = 5

Current Pods = 4

Controller Manager creates one new Pod.

---

## etcd

### Definition

A distributed key-value database storing all Kubernetes cluster information.

Stores:

- Pods
- Nodes
- Deployments
- Services
- ConfigMaps
- Secrets
- Namespaces

---

# 8. Worker Node Components

Each Worker Node contains:

```
Worker Node

├── Kubelet
├── Kube Proxy
├── Container Runtime
└── Pods
```

---

## Kubelet

### Definition

An agent running on every Worker Node.

### Responsibilities

- Starts Pods
- Stops Pods
- Monitors Pods
- Reports Node status

---

## Kube Proxy

### Definition

A networking component running on every Worker Node.

### Responsibilities

- Routes network traffic
- Performs load balancing
- Maintains network rules

---

## Container Runtime

### Definition

Software responsible for pulling images and running containers.

Examples

- containerd
- CRI-O

---

# 9. Kubernetes Workflow

```
User
 │
 │ kubectl
 ▼
API Server
 │
 ├──────────────► etcd
 │
 ▼
Scheduler
 │
 ▼
Select Worker Node
 │
 ▼
Kubelet
 │
 ▼
Container Runtime
 │
 ▼
Pod Starts
 │
 ▼
Application Running
 │
 ▼
Kube Proxy
 │
 ▼
User Accesses Service
```

---

# 10. Important Definitions

## kubectl

Command-line tool used to interact with Kubernetes.

Example

```bash
kubectl get pods
kubectl apply -f deployment.yaml
kubectl delete pod nginx
```

---

## YAML

A human-readable configuration file used to define Kubernetes resources.

Example

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx
```

---

## Scaling

Increasing or decreasing the number of Pods.

Types:

- Horizontal Scaling
- Vertical Scaling

---

## Load Balancing

Distributes traffic among multiple Pods.

---

## Self-Healing

Automatically replaces failed Pods or Containers.

---

## Rolling Update

Updates applications gradually without downtime.

---

## Rollback

Restores the previous stable application version.

---

## Desired State

The configuration defined by the user.

Example:

```
Replicas = 3
```

---

## Actual State

The current running condition of the Kubernetes cluster.

Example:

```
Running Pods = 2
```

Controller Manager makes the Actual State equal to the Desired State.

---

# 11. Summary Table

| Term | Definition |
|------|------------|
| Kubernetes | Container orchestration platform |
| Container | Package containing application and dependencies |
| Container Orchestration | Automated management of containers |
| Cluster | Collection of nodes |
| Control Plane | Brain of Kubernetes |
| Worker Node | Runs application Pods |
| Node | Physical or virtual machine |
| Pod | Smallest deployable unit |
| Deployment | Manages Pods |
| ReplicaSet | Maintains desired replicas |
| Service | Stable network endpoint |
| Namespace | Logical grouping of resources |
| API Server | Entry point for Kubernetes |
| Scheduler | Assigns Pods to Nodes |
| Controller Manager | Maintains desired state |
| etcd | Cluster database |
| Kubelet | Node agent |
| Kube Proxy | Network manager |
| Container Runtime | Runs containers |
| kubectl | Kubernetes CLI |
| YAML | Configuration file |
| Scaling | Increase/decrease Pods |
| Load Balancing | Distributes traffic |
| Self-Healing | Restarts failed Pods |
| Rolling Update | Updates applications without downtime |
| Rollback | Restores previous version |
| Desired State | User-defined configuration |
| Actual State | Current cluster status |

---

# Conclusion

Kubernetes is the industry-standard platform for managing containerized applications. It automates deployment, scaling, networking, and recovery while ensuring high availability and efficient resource utilization. Understanding its architecture—Control Plane, Worker Nodes, Pods, and core components such as the API Server, Scheduler, Controller Manager, etcd, Kubelet, and Kube Proxy—is essential for modern DevOps, cloud computing, and containerized application development.