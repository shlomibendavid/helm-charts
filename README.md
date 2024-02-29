# K8S-SSH

K8S-SSH used to allow ssh connection to a Kubernetes cluster nodes by injecting the user's ssh public keys. 

This chart bootstraps a [k8s-ssh](http://github.com/shlomibendavid/k8s-ssh) daemonset on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Install helm
- Create an override-values.yaml file and add all your user's and their ssh public keys

```yaml
users:
  user1: <user1_public_key>
  user2: <user2_public_key>
```

NOTE: you should replace the user1 and user2 and their public keys with the relevant once.

- Add the helm repo

```console
helm repo add k8s-ssh https://shlomibendavid.github.io/k8s-ssh
```

## Configuring

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing). To see all configurable options with detailed comments, visit the chart's [values.yaml](./values.yaml), or run these configuration commands:

```console
# Helm 3
$ helm show values .
```

## Template Generation

```console
# Helm 3
$ helm template k8s-ssh --values override-values.yaml .
```

## Installation

To install the helm chart

```console
helm install k8s-ssh k8s-ssh/k8s-ssh --version 1.0.2 --values override-values.yaml
```
