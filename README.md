# K8S-SSH

K8S-SSH used to allow ssh connection to a Kubernetes cluster nodes by injecting the user's ssh public keys. 

This chart bootstraps a [k8s-ssh](https://github.com/shlomibendavid/k8s-ssh) daemonset on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Configuring

See [Customizing the Chart Before Installing](https://helm.sh/docs/intro/using_helm/#customizing-the-chart-before-installing). To see all configurable options with detailed comments, visit the chart's [values.yaml](./values.yaml), or run these configuration commands:

```console
# Helm 3
$ helm show values .
```

## Template Generation

```console
# Helm 3
$ helm template k8s-ssh .
```
