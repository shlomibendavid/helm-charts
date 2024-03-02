# K8S-SSH

K8S-SSH used to allow ssh connection to a Kubernetes cluster nodes by injecting the user's ssh public keys.

This chart bootstraps a [k8s-ssh](https://artifacthub.io/packages/helm/k8s-ssh/k8s-ssh) daemonset on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Install [helm](https://helm.sh/docs/intro/install/)
- Add the helm repo

```console
helm repo add shlomibendavid https://shlomibendavid.github.io/k8s-ssh
```

## Configuring

- Create an `override-values.yaml` file and add all your user's and their ssh public keys

```yaml
users:
  <user1>: <user1_public_key>
```

NOTE: you should replace the `<user1>` and `<user1_public_key>` with your user and your public key.

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
helm install k8s-ssh shlomibendavid/k8s-ssh --version <version> --values override-values.yaml
```
