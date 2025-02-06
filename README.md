# community-catalog

apply this in your cluster
```
apiVersion: source.toolkit.fluxcd.io/v1
kind: GitRepository
metadata:
  name: community-catalog
  namespace: kommander
  labels:
    kommander.d2iq.io/gitapps-gitrepository-type: catalog
    kommander.d2iq.io/gitrepository-type: catalog
    kommander.d2iq.io/workspace-default-catalog-repository: "true"
spec:
  interval: 1m0s
  ref:
    branch: main
  timeout: 1m0s
  url: https://github.com/tuxtof/community-catalog.git
```
