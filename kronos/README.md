# Kronos

Kronos is a small Discord Bot.

## Parameters

| Name               | Description                                                              | Value              |
| ------------------ | ------------------------------------------------------------------------ | ------------------ |
| `image.repository` | Image repository                                                         | `feleuxens/kronos` |
| `image.pullPolicy` | Image pull policy                                                        | `IfNotPresent`     |
| `image.tag`        | Image tag. Overrides the image tag whose default is the chart appVersion | `""`               |
| `imagePullSecrets` | Image pull secrets needed when pulling from private repository           | `[]`               |
| `nameOverride`     | Name override                                                            | `""`               |
| `fullnameOverride` | Fullname override                                                        | `""`               |
| `podAnnotations`   | Pod annotations                                                          | `{}`               |
| `resources`        | CPU and memory requests/limits                                           | `{}`               |
| `nodeSelector`     | Node labels for pod assignment                                           | `{}`               |
| `tolerations`      | Toleration labels for pod assignment                                     | `[]`               |
| `affinity`         | Affinity settings for pod assignment                                     | `{}`               |
