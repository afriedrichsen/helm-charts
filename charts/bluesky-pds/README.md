# bluesky-pds

A Helm chart for BlueSky Social PDS server

## Features

- Credential

## Deployment

1. Add helm repo

```
helm repo add afriedrichsen-charts https://afriedrichsen.github.io/helm-charts
```

2. Deploy helm chart

```
helm install afriedrichsen-charts/bluesky-pds \
--set global.hostname="<YOUR BLUESKY HOSTNAME/DOMAIN>" \
```

3. Verify service is available inside cluster at port `3000`

```
kubectl -n <TARGET NAMESPACE> get svc
kubectl -n <TARGET NAMESPACE> port-forward svc/bluesky-pds 3000:3000
```

## Uninstall

Use helm to uninstall the chart

```
helm -n <TARGET_NAMESPACE> uninstall bluesky-pds
```

## Maintainer

- afriedrichsen
