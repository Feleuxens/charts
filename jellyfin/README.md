# Jellyfin

Jellyfin is the volunteer-built media solution that puts you in control of your media.

## Parameters

### General settings

| Name                               | Description                          | Value               |
| ---------------------------------- | ------------------------------------ | ------------------- |
| `replicaCount`                     | Replica count                        | `1`                 |
| `image.repository`                 | The Docker image to use              | `jellyfin/jellyfin` |
| `image.pullPolicy`                 | Pull policy                          | `IfNotPresent`      |
| `image.tag`                        | Image tag. Defaults to Chart version | `""`                |
| `imagePullSecrets`                 |                                      | `[]`                |
| `nameOverride`                     |                                      | `""`                |
| `fullnameOverride`                 |                                      | `""`                |
| `resources`                        | Set resources                        | `{}`                |
| `nodeSelector`                     |                                      | `{}`                |
| `tolerations`                      |                                      | `[]`                |
| `affinity`                         |                                      | `{}`                |
| `podAnnotations`                   |                                      | `{}`                |
| `podSecurityContext`               |                                      | `{}`                |
| `securityContext`                  |                                      | `{}`                |
| `service.type`                     | Service type                         | `ClusterIP`         |
| `service.port`                     | Service port                         | `8096`              |
| `service.annotations`              | Additional service annotations       | `{}`                |
| `service.labels`                   | Additional service labels            | `{}`                |
| `service.clusterIP`                | Specify explicit cluster IP          | `nil`               |
| `service.loadBalancerIP`           | Specify explicit load balancer IP    | `nil`               |
| `service.loadBalancerSourceRanges` | Specify load balancer source range   | `[]`                |
| `service.externalIPs`              | Specify external IP                  | `[]`                |
| `service.externalTrafficPolicy`    | External traffic policy              | `Cluster`           |

### Discovery Service

| Name                                        | Description                                                  | Value   |
| ------------------------------------------- | ------------------------------------------------------------ | ------- |
| `enableDLNA`                                | Enables DLNA port. Creates a loadbalancer service            | `false` |
| `enableLocalDiscovery`                      | Enables local discovery port. Creates a loadbalancer service | `false` |
| `discoveryService.annotations`              | Annotations for the discovery service                        | `{}`    |
| `discoveryService.labels`                   | Labels for the discovery service                             | `{}`    |
| `discoveryService.loadBalancerIP`           | Specify loadbalancer IP                                      | `nil`   |
| `discoveryService.loadBalancerSourceRanges` | Specify loadbalancer source range                            | `[]`    |

### Ingress

| Name                  | Description                              | Value   |
| --------------------- | ---------------------------------------- | ------- |
| `ingress.enabled`     | Enable ingress                           | `false` |
| `ingress.className`   | Ingress class name                       | `nginx` |
| `ingress.annotations` | Ingress annotations                      | `{}`    |
| `ingress.hosts`       | Hosts of the ingress record              | `[]`    |
| `ingress.tls`         | List of secrets with the TLS certificate | `[]`    |

### Persistence

| Name                               | Description                                                                    | Value               |
| ---------------------------------- | ------------------------------------------------------------------------------ | ------------------- |
| `persistence.config.enabled`       | Enable persistence for the config                                              | `false`             |
| `persistence.config.storageClass`  | Choose storage class for the PVC. "~" will choose the default storage provider | `~`                 |
| `persistence.config.existingClaim` | Specify an existing claim                                                      | `nil`               |
| `persistence.config.accessModes`   | Access modes of the PVC                                                        | `["ReadWriteOnce"]` |
| `persistence.config.size`          | Size of the PVC                                                                | `1Gi`               |
| `persistence.media.enabled`        | Enable persistence for the config                                              | `false`             |
| `persistence.media.storageClass`   | Choose storage class for the PVC. "~" will choose the default storage provider | `~`                 |
| `persistence.media.existingClaim`  | Specify an existing claim                                                      | `nil`               |
| `persistence.media.accessModes`    | Access modes of the PVC                                                        | `["ReadWriteOnce"]` |
| `persistence.media.size`           | Size of the PVC                                                                | `10Gi`              |
| `extraVolumes`                     | Specify extra volumes                                                          | `[]`                |
| `extraVolumeMounts`                | Specify extra volume mounts                                                    | `[]`                |
