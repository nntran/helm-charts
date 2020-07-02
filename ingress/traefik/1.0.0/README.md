# Traefik Helm Chart

Traefik is an [open-source](https://github.com/containous/traefik) Edge Router that makes publishing your services a fun and easy experience. It receives requests on behalf of your system and finds out which components are responsible for handling them.

See more [...](https://docs.traefik.io)

## Clone the git repository

```sh
git clone https://github.com/nntran/rancher-charts charts
```

## Create namespace

Create `proxy` namespace if not exists.

```
kubectl create namespace proxy
```

## Dry run

```sh
helm install trefik  ./ingress/traefik/1.0.0 -n proxy --debug --dry-run
```

## Install

```sh
helm install trefik ./ingress/traefik/1.0.0 -n proxy
```

## Test

```sh
helm test trefik -n proxy
```

Output example :

```

```

## Uninstall

```sh
helm uninstall trefik -n proxy --debug
```

Output example:

```

```
