# trustrification-operator

# Red Hat Trusted Content - The Trustification Operator
The Trustification Operator allows deployment of the Trustification solution on a Kubernetes (or k8s compatible) cluster.

## Requirements

### Hardware [WIP]

20GB RAM
4 Cpus/VCpus
40 Storage space

### Software
* The following are required 
* 8s v1.22+ or OpenShift 4.9+
* Operator Lifecycle Manager (OLM) support
* Ingress support
* Network policy support
* Persistent Storage

Although there are multiple solutions to run a local K8s cluster such as K3s, MicroK8s, kind, Minikube, CRC. Only Minikube and CRC (Codre Ready Container) solutions are going to be supported.

## Services being deployed (not exhaustive yet)

The Trustification Operator, will deploy
* The GUAC stack 

The Trustification services:
* Bombastic
* Vexination
* V11y
* Exhort

The Trustification collector services:
* Collectorist API
* Vexination OSV
* Bombastic NVD - On hold for now
* V11y Snyk

The Trustification indexing services:
* Vexination indexer
* Bombastic indexer
* V11y ind

### Minikube Quickstart
```
minikube config set memory 10240
minikube config set cpus 4
minikube start --addons=dashboard --addons=ingress --addons=olm
```
