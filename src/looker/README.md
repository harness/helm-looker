# ng-custom-dashboards

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v1.52.10](https://img.shields.io/badge/AppVersion-v1.52.10-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 2.x.x |
| https://harness.github.io/helm-common | harness-common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| authSecrets.acl.key | string | `"AUTH_ACCESS_CONTROL_SECRET"` |  |
| authSecrets.acl.name | string | `"harness-secrets"` |  |
| authSecrets.ccm.key | string | `"AUTH_CCM_SECRET"` |  |
| authSecrets.ccm.name | string | `"harness-secrets"` |  |
| authSecrets.cgManager.key | string | `"AUTH_CG_MANAGER_SECRET"` |  |
| authSecrets.cgManager.name | string | `"harness-secrets"` |  |
| authSecrets.identityService.key | string | `"AUTH_IDENTITY_SERVICE_SECRET"` |  |
| authSecrets.identityService.name | string | `"harness-secrets"` |  |
| authSecrets.ngManager.key | string | `"AUTH_NG_MANAGER_SECRET"` |  |
| authSecrets.ngManager.name | string | `"harness-secrets"` |  |
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| config.customerFolderId | string | `"6"` | folder ID of the 'CUSTOMER' folder in looker |
| config.env | string | `""` | deprecated |
| config.lookerApiVersion | string | `"4.0"` | looker sdk param |
| config.lookerHost | string | `"harness-looker"` | hostname of your looker install |
| config.lookerTimeout | string | `"120"` | looker sdk param |
| config.lookerVerifySsl | string | `"false"` | looker sdk param |
| config.modelPrefix | string | `""` | if you have configured models with a prefix enter it here |
| config.ootbFolderId | string | `"7"` | folder ID of the 'OOTB' folder in looker |
| config.redisHost | string | `"harness-redis-master"` | hostname of your redis install |
| config.redisPort | string | `"6379"` | port of your redis install |
| fullnameOverride | string | `""` |  |
| global.airgap | string | `"false"` |  |
| global.loadbalancerURL | string | `""` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"harness/dashboard-service-signed"` |  |
| image.tag | string | `"v1.52.14"` |  |
| lookerSecrets.clientId.key | string | `"LOOKERSDK_CLIENT_ID"` |  |
| lookerSecrets.clientId.name | string | `"harness-secrets"` |  |
| lookerSecrets.clientSecret.key | string | `"LOOKERSDK_CLIENT_SECRET"` |  |
| lookerSecrets.clientSecret.name | string | `"harness-secrets"` |  |
| lookerSecrets.secret.key | string | `"SECRET"` |  |
| lookerSecrets.secret.name | string | `"harness-secrets"` |  |
| maxSurge | int | `1` |  |
| maxUnavailable | int | `0` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | int | `1` |  |
| resources.limits.memory | string | `"1536Mi"` |  |
| resources.requests.cpu | int | `1` |  |
| resources.requests.memory | string | `"768Mi"` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `65534` |  |
| service.port | int | `5000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `"harness-default"` |  |
| tolerations | list | `[]` |  |
