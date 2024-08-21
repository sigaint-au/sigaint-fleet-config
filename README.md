# Fleet Config

Fleet configuration for `Sigaint` clusters.

## Requirements
### External Secrets
You need to create the `doppler-secret` in the `external-secrets` namespace before you deploy anything.

* https://external-secrets.io/latest/provider/doppler/
* https://dashboard.doppler.com

```
apiVersion: v1
kind: Secret
metadata:
  name: doppler-token-auth-api
  namespace: external-secrets
type: Opaque
stringData:
  dopplerToken: "<token>"
```

### Cert Manager
You need to put the Cloudflare API token into the `prd/CLOUDFLARE_API_TOKEN` secret in doppler.

## Deployment
Create the `fleet-config.yaml` git repo.