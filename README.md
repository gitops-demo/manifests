# manifests
Single Source of Truth (Manifest files) for user applications

## Branches
* `dev`: Its contents will be deployed on the development env
* `prd`: Its contents will be deployed on the production env

## Contents
### app-a
* Template by helm

### app-b
* Template by kustomize

## Note
* Normally, you should choose one template engine from helm or kustomize. The sample contains both of helm and kustomize for ONLY illustration.

## Appendix
Original files

`dev-secret.yaml`

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: dev-app-b # NOTE: You must concern kustomize namePrefix
data:
  APPB_VERYSECRETMESSAGE: dmVyeS1zZWNyZXQtcGFzc3dvcmQ=
```

`prd-secret.yaml`

```yaml
apiVersion: v1
kind: Secret
metadata:
  name: prd-app-b # NOTE: You must concern kustomize namePrefix
data:
  APPB_VERYSECRETMESSAGE: dmVyeS1zZWNyZXQtcGFzc3dvcmQtZm9yLXByZA==
```
