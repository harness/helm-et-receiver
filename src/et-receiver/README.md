# et-receiver

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `5` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| env.config.DB_TYPE | string | `"mysql"` |  |
| env.config.DB_URL | string | `"mysql-gcp:3306"` |  |
| env.config.DB_USER | string | `"overops"` |  |
| env.config.JVM_HEAPSIZE | string | `"1600m"` |  |
| env.secrets.DB_PASS | string | `"overops"` |  |
| et.hikari.connectionTimeout | int | `60000` |  |
| et.hikari.maximumPoolSize | int | `10` |  |
| et.logLevel | string | `"INFO"` |  |
| et.redis.host | string | `"redis-gcp"` |  |
| et.redis.port | int | `6379` |  |
| et.redis.streamLength | int | `500` |  |
| et.redis.trimCronExpression | string | `"@hourly"` |  |
| et.redisQueue.type | string | `"hit"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"us.gcr.io/overops-play/overops/et-receiver"` |  |
| image.tag | string | `"5.2.3-SNAPSHOT-309"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].backend.serviceName | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].backend.servicePort | int | `9191` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| initContainers.check.image.repository | string | `"busybox"` |  |
| initContainers.check.image.tag | string | `"1.33.1"` |  |
| initContainers.postgresql.image.repository | string | `"bitnami/postgresql"` |  |
| initContainers.postgresql.image.tag | string | `"11.10.0-debian-10-r24"` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `40` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| maxSurge | string | `"100%"` |  |
| maxUnavailable | int | `0` |  |
| nameOverride | string | `""` |  |
| namespace.name | string | `"overops-snapshot"` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `35` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | int | `2` |  |
| resources.limits.memory | string | `"2Gi"` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"2Gi"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `9191` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| startupProbe.enabled | bool | `true` |  |
| startupProbe.failureThreshold | int | `10` |  |
| startupProbe.initialDelaySeconds | int | `40` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| tolerations | list | `[]` |  |
