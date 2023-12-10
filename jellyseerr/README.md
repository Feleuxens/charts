# Jellyfin

Jellyseerr is a free and open source fork of Overseerr for managing requests for your media library.

## Parameters

### General

| Name                               | Description                                                                    | Value                    |
| ---------------------------------- | ------------------------------------------------------------------------------ | ------------------------ |
| `replicaCount`                     | Replica count                                                                  | `1`                      |
| `image.repository`                 | The Docker image to use                                                        | `fallenbagel/jellyseerr` |
| `image.pullPolicy`                 | Pull policy                                                                    | `IfNotPresent`           |
| `image.tag`                        | Image tag. Defaults to Chart version                                           | `""`                     |
| `imagePullSecrets`                 |                                                                                | `[]`                     |
| `nameOverride`                     |                                                                                | `""`                     |
| `fullnameOverride`                 |                                                                                | `""`                     |
| `resources`                        | Set resources                                                                  | `{}`                     |
| `nodeSelector`                     |                                                                                | `{}`                     |
| `tolerations`                      |                                                                                | `[]`                     |
| `affinity`                         |                                                                                | `{}`                     |
| `podAnnotations`                   |                                                                                | `{}`                     |
| `podSecurityContext`               |                                                                                | `{}`                     |
| `securityContext`                  |                                                                                | `{}`                     |
| `service.type`                     | Service type                                                                   | `ClusterIP`              |
| `service.port`                     | Service port                                                                   | `5055`                   |
| `service.annotations`              | Additional service annotations                                                 | `{}`                     |
| `service.labels`                   | Additional service labels                                                      | `{}`                     |
| `service.clusterIP`                | Specify explicit cluster IP                                                    | `nil`                    |
| `service.loadBalancerIP`           | Specify explicit load balancer IP                                              | `nil`                    |
| `service.loadBalancerSourceRanges` | Specify load balancer source range                                             | `[]`                     |
| `service.externalIPs`              | Specify external IP                                                            | `[]`                     |
| `service.externalTrafficPolicy`    | External traffic policy                                                        | `Cluster`                |
| `persistence.storageClass`         | Choose storage class for the PVC. "~" will choose the default storage provider | `~`                      |
| `persistence.existingClaim`        | Specify an existing claim                                                      | `nil`                    |
| `persistence.accessModes`          | Access modes of the PVC                                                        | `["ReadWriteOnce"]`      |
| `persistence.size`                 | Size of the PVC                                                                | `15Gi`                   |
| `extraVolumes`                     | Specify extra volumes                                                          | `[]`                     |
| `extraVolumeMounts`                | Specify extra volume mounts                                                    | `[]`                     |
| `env.logLevel`                     | Set the log level of jellyseerr                                                | `info`                   |
| `env.timezone`                     | Set the timezone                                                               | `Europe/Berlin`          |
| `env.jellyfinType`                 | If you use emby set this to "emby"                                             | `jellyfin`               |

### Ingress

| Name                  | Description                              | Value   |
| --------------------- | ---------------------------------------- | ------- |
| `ingress.enabled`     | Enable ingress                           | `false` |
| `ingress.className`   | Ingress class name                       | `""`    |
| `ingress.annotations` | Ingress annotations                      | `{}`    |
| `ingress.hosts`       | Hosts of the ingress record              | `[]`    |
| `ingress.tls`         | List of secrets with the TLS certificate | `[]`    |
