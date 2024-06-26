# grafana-beyla

![Version: 1.5.2](https://img.shields.io/badge/Version-1.5.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.5.2](https://img.shields.io/badge/AppVersion-1.5.2-informational?style=flat-square)

A Helm chart for Kubernetes

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Vitaly Fedorov | <obsessionsys@gmail.com> |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Affinity for pod assignment. See: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/#affinity-and-anti-affinity |
| annotations | object | `{}` | General annotation for the daemonset |
| config | string | Dynamically generated beyla configmap | Beyla configuration file contents |
| extraEnvs | list | `[]` | Extra environment variables to add |
| fullnameOverride | string | `""` | Overrides the chart's computed fullname |
| hostAliases | list | `[]` | hostAliases to add |
| hostPID | bool | `true` | Mandatory for eBPF probes |
| image.pullPolicy | string | `"IfNotPresent"` | pullPolicy to use for pulling the image |
| image.repository | string | `"grafana/beyla"` | Repository to pull from |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` | Overrides the chart's name |
| nodeSelector | object | `{}` | Node labels for pod assignment. See: https://kubernetes.io/docs/user-guide/node-selection/ |
| otlp.endpoint | string | `"http://localhost"` | For correct operation, this endpoint must be installed and point to the opentelemtry collector service or ingress |
| otlp.headers | object | `{}` | Headers for OTLP Collector Example: Authorization=Basic ...rest of the secret header value... |
| otlp.insecure | bool | `false` |  |
| otlp.protocol | string | `nil` | Protocol OTLP Collector (http or grpc) |
| podAnnotations | object | `{}` | Pod Annotations |
| podLabels | object | `{}` | Pod (extra) Labels |
| podSecurityContext | object | `{}` | podSecurityContext  |
| resources | object | `{}` |  |
| securityContext.privileged | bool | `true` | Defaults to privileged = true |
| securityContext.readOnlyRootFilesystem | bool | `true` |  |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.automount | bool | `true` | Automatically mount a ServiceAccount's API credentials? |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | If not set and create is true, a name is generated using the fullname template |
| terminationMessagePolicy | string | `nil` | See https://kubernetes.io/docs/tasks/debug/debug-application/determine-reason-pod-failure/ |
| tolerations | list | `[]` | Tolerations for pod assignment. See: https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| volumeMounts | list | `[]` | Additional volumeMounts on the output Deployment definition. |
| volumes | list | `[]` | Additional volumes on the output Deployment definition. |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.8.1](https://github.com/norwoodj/helm-docs/releases/v1.8.1)
