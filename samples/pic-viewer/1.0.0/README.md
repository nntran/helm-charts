# Picture Viewer Helm Chart

A sample application for Docker training

## Clone the git repository

```sh
git clone https://github.com/nntran/rancher-charts charts
```

## Create namespace

Create `samples` namespace if not exists.

```
kubectl create namespace samples
```

## Dry run

```sh
helm install  pic-viewer ./charts/samples/pic-viewer/1.0.0 -n samples --debug --dry-run
```

## Install

```sh
helm install pic-viewer ./charts/samples/pic-viewer/1.0.0 -n samples
```

## Test

```sh
helm test pic-viewer -n samples
```

Output example :

```
Pod pic-viewer-test-connection pending
Pod pic-viewer-test-connection pending
Pod pic-viewer-test-connection succeeded
NAME: pic-viewer
LAST DEPLOYED: Wed Jul  1 16:34:40 2020
NAMESPACE: samples
STATUS: deployed
REVISION: 1
TEST SUITE:     pic-viewer-test-connection
Last Started:   Wed Jul  1 16:36:14 2020
Last Completed: Wed Jul  1 16:36:22 2020
Phase:          Succeeded
NOTES:
1. Get the application URL by running these commands:
  http://pv.dev.lan/
```

## Uninstall

```sh
helm uninstall pic-viewer -n samples --debug
```

Output example:

```
uninstall.go:91: [debug] uninstall: Deleting pic-viewer
client.go:220: [debug] Starting delete for "pic-viewer" Ingress
client.go:220: [debug] Starting delete for "pic-viewer" Service
client.go:220: [debug] Starting delete for "pic-viewer" Deployment
uninstall.go:124: [debug] purge requested for pic-viewer
release "pic-viewer" uninstalled
```
