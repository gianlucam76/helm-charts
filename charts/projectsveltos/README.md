# projectsveltos

![Version: 0.47.1](https://img.shields.io/badge/Version-0.47.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.47.0](https://img.shields.io/badge/AppVersion-0.47.0-informational?style=flat-square)

Projectsveltos helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| global.useDigest | bool | `false` |  |
| global.imagePullSecrets | list | `[]` |  |
| accessManager.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| accessManager.manager.args[1] | string | `"--v=5"` |  |
| accessManager.manager.extraArgs | object | `{}` |  |
| accessManager.manager.extraEnv | list | `[]` |  |
| accessManager.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| accessManager.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| accessManager.manager.image.repository | string | `"docker.io/projectsveltos/access-manager"` |  |
| accessManager.manager.image.tag | string | `"v0.47.0"` |  |
| accessManager.manager.image.digest | string | `"sha256:c4babf5fbc2f2d7030ca1942b5f7aea8c7fe98e566e9a30d3b894f05b34643e0"` |  |
| accessManager.manager.resources.limits.cpu | string | `"500m"` |  |
| accessManager.manager.resources.limits.memory | string | `"512Mi"` |  |
| accessManager.manager.resources.requests.cpu | string | `"10m"` |  |
| accessManager.manager.resources.requests.memory | string | `"128Mi"` |  |
| accessManager.nodeSelector | object | `{}` |  |
| accessManager.podSecurityContext.runAsNonRoot | bool | `true` |  |
| accessManager.replicas | int | `1` |  |
| accessManager.tolerations | list | `[]` |  |
| accessManager.serviceAccount.annotations | object | `{}` |  |
| addonController.controller.args[0] | string | `"--diagnostics-address=:8443"` |  |
| addonController.controller.args[1] | string | `"--report-mode=0"` |  |
| addonController.controller.args[2] | string | `"--shard-key="` |  |
| addonController.controller.args[3] | string | `"--v=5"` |  |
| addonController.controller.args[4] | string | `"--version=v0.47.0"` |  |
| addonController.controller.extraArgs | object | `{}` |  |
| addonController.controller.argsAgentMgmtCluster[0] | string | `"--diagnostics-address=:8443"` |  |
| addonController.controller.argsAgentMgmtCluster[1] | string | `"--report-mode=0"` |  |
| addonController.controller.argsAgentMgmtCluster[2] | string | `"--agent-in-mgmt-cluster"` |  |
| addonController.controller.argsAgentMgmtCluster[3] | string | `"--shard-key="` |  |
| addonController.controller.argsAgentMgmtCluster[4] | string | `"--v=5"` |  |
| addonController.controller.argsAgentMgmtCluster[5] | string | `"--version=v0.47.0"` |  |
| addonController.controller.extraArgsAgentMgmtCluster | object | `{}` |  |
| addonController.controller.extraEnv | list | `[]` |  |
| addonController.controller.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| addonController.controller.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| addonController.controller.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| addonController.controller.image.repository | string | `"docker.io/projectsveltos/addon-controller"` |  |
| addonController.controller.image.tag | string | `"v0.47.0"` |  |
| addonController.controller.image.digest | string | `"sha256:9604dafd4b1903af99a5929e4bc2a19fb0ccaf6b2b5f81bc8bf2fc3a510d9ebc"` |  |
| addonController.controller.resources.requests.memory | string | `"512Mi"` |  |
| addonController.driftDetectionManagerPatchConfigMap.name | string | `"drift-detection-config"` |  |
| addonController.driftDetectionManagerPatchConfigMap.data | object | `{}` |  |
| addonController.podSecurityContext.runAsNonRoot | bool | `true` |  |
| addonController.ports[0].name | string | `"metrics"` |  |
| addonController.ports[0].port | int | `80` |  |
| addonController.ports[0].protocol | string | `"TCP"` |  |
| addonController.ports[0].targetPort | int | `8443` |  |
| addonController.nodeSelector | object | `{}` |  |
| addonController.replicas | int | `1` |  |
| addonController.tolerations | list | `[]` |  |
| addonController.serviceAccount.annotations | object | `{}` |  |
| addonController.type | string | `"ClusterIP"` |  |
| classifierManager.agentPatchConfigMap.name | string | `"sveltos-agent-config"` |  |
| classifierManager.agentPatchConfigMap.data | object | `{}` |  |
| classifierManager.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| classifierManager.manager.args[1] | string | `"--report-mode=0"` |  |
| classifierManager.manager.args[2] | string | `"--shard-key="` |  |
| classifierManager.manager.args[3] | string | `"--v=5"` |  |
| classifierManager.manager.args[4] | string | `"--version=v0.47.0"` |  |
| classifierManager.manager.extraArgs | object | `{}` |  |
| classifierManager.manager.argsAgentMgmtCluster[0] | string | `"--diagnostics-address=:8443"` |  |
| classifierManager.manager.argsAgentMgmtCluster[1] | string | `"--report-mode=0"` |  |
| classifierManager.manager.argsAgentMgmtCluster[2] | string | `"--agent-in-mgmt-cluster"` |  |
| classifierManager.manager.argsAgentMgmtCluster[3] | string | `"--shard-key="` |  |
| classifierManager.manager.argsAgentMgmtCluster[4] | string | `"--v=5"` |  |
| classifierManager.manager.argsAgentMgmtCluster[5] | string | `"--version=v0.47.0"` |  |
| classifierManager.manager.extraArgsAgentMgmtCluster | object | `{}` |  |
| classifierManager.manager.extraEnv | list | `[]` |  |
| classifierManager.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| classifierManager.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| classifierManager.manager.image.repository | string | `"docker.io/projectsveltos/classifier"` |  |
| classifierManager.manager.image.tag | string | `"v0.47.0"` |  |
| classifierManager.manager.image.digest | string | `"sha256:1fcbb2c9f7ca9b7675790857471848271fa9a2aff3bcb5fedf16526288b9da74"` |  |
| classifierManager.manager.resources.limits.cpu | string | `"500m"` |  |
| classifierManager.manager.resources.limits.memory | string | `"512Mi"` |  |
| classifierManager.manager.resources.requests.cpu | string | `"100m"` |  |
| classifierManager.manager.resources.requests.memory | string | `"128Mi"` |  |
| classifierManager.nodeSelector | object | `{}` |  |
| classifierManager.podSecurityContext.runAsNonRoot | bool | `true` |  |
| classifierManager.replicas | int | `1` |  |
| classifierManager.tolerations | list | `[]` |  |
| classifierManager.serviceAccount.annotations | object | `{}` |  |
| conversionWebhook.podSecurityContext.runAsNonRoot | bool | `true` |  |
| conversionWebhook.replicas | int | `1` |  |
| conversionWebhook.sveltosWebhook.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| conversionWebhook.sveltosWebhook.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| conversionWebhook.sveltosWebhook.image.repository | string | `"docker.io/projectsveltos/webhook-conversion"` |  |
| conversionWebhook.sveltosWebhook.image.tag | string | `"v0.47.0"` |  |
| conversionWebhook.sveltosWebhook.image.digest | string | `"sha256:12bd3a7cf1195cec38f4c905c9d6c04f1bfef25574fc1977fb51f42347f73842"` |  |
| conversionWebhook.sveltosWebhook.resources.limits.cpu | string | `"500m"` |  |
| conversionWebhook.sveltosWebhook.resources.limits.memory | string | `"512Mi"` |  |
| conversionWebhook.sveltosWebhook.resources.requests.cpu | string | `"10m"` |  |
| conversionWebhook.sveltosWebhook.resources.requests.memory | string | `"128Mi"` |  |
| conversionWebhook.nodeSelector | object | `{}` |  |
| conversionWebhook.tolerations | list | `[]` |  |
| driftDetectionManager.serviceAccount.annotations | object | `{}` |  |
| eventManager.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| eventManager.manager.args[1] | string | `"--shard-key="` |  |
| eventManager.manager.args[2] | string | `"--v=5"` |  |
| eventManager.manager.args[3] | string | `"--version=v0.47.0"` |  |
| eventManager.manager.extraArgs | object | `{}` |  |
| eventManager.manager.extraEnv | list | `[]` |  |
| eventManager.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| eventManager.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| eventManager.manager.image.repository | string | `"docker.io/projectsveltos/event-manager"` |  |
| eventManager.manager.image.tag | string | `"v0.47.0"` |  |
| eventManager.manager.image.digest | string | `"sha256:1accd3738a02a2a30be240e8a0e586a2b059e5b5ccaf783f2c35a3da2f843185"` |  |
| eventManager.manager.resources.limits.cpu | string | `"500m"` |  |
| eventManager.manager.resources.limits.memory | string | `"512Mi"` |  |
| eventManager.manager.resources.requests.cpu | string | `"10m"` |  |
| eventManager.manager.resources.requests.memory | string | `"128Mi"` |  |
| eventManager.nodeSelector | object | `{}` |  |
| eventManager.podSecurityContext.runAsNonRoot | bool | `true` |  |
| eventManager.replicas | int | `1` |  |
| eventManager.tolerations | list | `[]` |  |
| eventManager.serviceAccount.annotations | object | `{}` |  |
| hcManager.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| hcManager.manager.args[1] | string | `"--shard-key="` |  |
| hcManager.manager.args[2] | string | `"--v=5"` |  |
| hcManager.manager.args[3] | string | `"--version=v0.47.0"` |  |
| hcManager.manager.extraArgs | object | `{}` |  |
| hcManager.manager.extraEnv | list | `[]` |  |
| hcManager.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| hcManager.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| hcManager.manager.image.repository | string | `"docker.io/projectsveltos/healthcheck-manager"` |  |
| hcManager.manager.image.tag | string | `"v0.47.0"` |  |
| hcManager.manager.image.digest | string | `"sha256:fe4bd1695ec2ebe33da4aa51e097bbc7f1e1377e4a8e0d79300166a36cd7a9c0"` |  |
| hcManager.manager.resources.limits.cpu | string | `"500m"` |  |
| hcManager.manager.resources.limits.memory | string | `"512Mi"` |  |
| hcManager.manager.resources.requests.cpu | string | `"10m"` |  |
| hcManager.manager.resources.requests.memory | string | `"128Mi"` |  |
| hcManager.nodeSelector | object | `{}` |  |
| hcManager.podSecurityContext.runAsNonRoot | bool | `true` |  |
| hcManager.replicas | int | `1` |  |
| hcManager.tolerations | list | `[]` |  |
| hcManager.serviceAccount.annotations | object | `{}` |  |
| kubernetesClusterDomain | string | `"cluster.local"` |  |
| registerMgmtCluster.serviceAccount.annotations | object | `{}` |  |
| registerMgmtClusterJob.backoffLimit | int | `4` |  |
| registerMgmtClusterJob.registerMgmtCluster.args[0] | string | `"--labels="` |  |
| registerMgmtClusterJob.registerMgmtCluster.args[1] | string | `"--service-account-token=false"` |  |
| registerMgmtClusterJob.registerMgmtCluster.extraArgs | object | `{}` |  |
| registerMgmtClusterJob.registerMgmtCluster.extraEnv | list | `[]` |  |
| registerMgmtClusterJob.registerMgmtCluster.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| registerMgmtClusterJob.registerMgmtCluster.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| registerMgmtClusterJob.registerMgmtCluster.image.repository | string | `"docker.io/projectsveltos/register-mgmt-cluster"` |  |
| registerMgmtClusterJob.registerMgmtCluster.image.tag | string | `"v0.47.0"` |  |
| registerMgmtClusterJob.registerMgmtCluster.image.digest | string | `"sha256:f1e6e312991267add25e490d90b54d15fe3e5e2ca44d93aeea1ed6a8a5dce6ab"` |  |
| registerMgmtClusterJob.registerMgmtCluster.imagePullPolicy | string | `"IfNotPresent"` |  |
| registerMgmtClusterJob.registerMgmtCluster.resources.requests.memory | string | `"128Mi"` |  |
| scManager.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| scManager.manager.args[1] | string | `"--shard-key="` |  |
| scManager.manager.args[2] | string | `"--v=5"` |  |
| scManager.manager.extraArgs | object | `{}` |  |
| scManager.manager.extraEnv | list | `[]` |  |
| scManager.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| scManager.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| scManager.manager.image.repository | string | `"docker.io/projectsveltos/sveltoscluster-manager"` |  |
| scManager.manager.image.tag | string | `"v0.47.0"` |  |
| scManager.manager.image.digest | string | `"sha256:126d1a2efcb927189f5b36051928401e93d183608a2e837a8d42c81c5bc3df33"` |  |
| scManager.manager.resources.limits.cpu | string | `"500m"` |  |
| scManager.manager.resources.limits.memory | string | `"512Mi"` |  |
| scManager.manager.resources.requests.cpu | string | `"10m"` |  |
| scManager.manager.resources.requests.memory | string | `"128Mi"` |  |
| scManager.nodeSelector | object | `{}` |  |
| scManager.podSecurityContext.runAsNonRoot | bool | `true` |  |
| scManager.ports[0].name | string | `"metrics"` |  |
| scManager.ports[0].port | int | `80` |  |
| scManager.ports[0].protocol | string | `"TCP"` |  |
| scManager.ports[0].targetPort | int | `8443` |  |
| scManager.replicas | int | `1` |  |
| scManager.tolerations | list | `[]` |  |
| scManager.serviceAccount.annotations | object | `{}` |  |
| scManager.type | string | `"ClusterIP"` |  |
| shardController.extraEnv | list | `[]` |  |
| shardController.manager.args[0] | string | `"--diagnostics-address=:8443"` |  |
| shardController.manager.args[1] | string | `"--v=5"` |  |
| shardController.manager.args[2] | string | `"--report-mode=0"` |  |
| shardController.manager.extraArgs | object | `{}` |  |
| shardController.manager.argsAgentMgmtCluster[0] | string | `"--diagnostics-address=:8443"` |  |
| shardController.manager.argsAgentMgmtCluster[1] | string | `"--report-mode=0"` |  |
| shardController.manager.argsAgentMgmtCluster[2] | string | `"--agent-in-mgmt-cluster"` |  |
| shardController.manager.argsAgentMgmtCluster[3] | string | `"--v=5"` |  |
| shardController.manager.extraArgsAgentMgmtCluster | object | `{}` |  |
| shardController.manager.extraEnv | list | `[]` |  |
| shardController.manager.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| shardController.manager.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| shardController.manager.image.repository | string | `"docker.io/projectsveltos/shard-controller"` |  |
| shardController.manager.image.tag | string | `"v0.47.0"` |  |
| shardController.manager.image.digest | string | `"sha256:eaab3824acfaf8be31b2b9640b7fce01325d4051d2f20013c5601ec945dfdf04"` |  |
| shardController.manager.resources.limits.cpu | string | `"500m"` |  |
| shardController.manager.resources.limits.memory | string | `"512Mi"` |  |
| shardController.manager.resources.requests.cpu | string | `"10m"` |  |
| shardController.manager.resources.requests.memory | string | `"128Mi"` |  |
| shardController.nodeSelector | object | `{}` |  |
| shardController.podSecurityContext.runAsNonRoot | bool | `true` |  |
| shardController.replicas | int | `1` |  |
| shardController.tolerations | list | `[]` |  |
| shardController.serviceAccount.annotations | object | `{}` |  |
| sveltosAgentManager.serviceAccount.annotations | object | `{}` |  |
| prometheus.enabled | bool | `false` |  |
| agent.managementCluster | bool | `false` |  |
| telemetry.disabled | bool | `false` |  |
| webhookService.ports[0].port | int | `443` |  |
| webhookService.ports[0].protocol | string | `"TCP"` |  |
| webhookService.ports[0].targetPort | int | `9443` |  |
| webhookService.type | string | `"ClusterIP"` |  |
| webhook.conversion | bool | `false` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
