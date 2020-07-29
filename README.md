# Unofficial Upsource Helm Chart

Helm chart for deployment of JetBrains Upsource in Kubernetes.

## Installing helm chart

```bash
helm repo add upsource https://includerandom.github.io/upsource-helm
helm repo update
helm install upsource upsource/upsource
```

## Chart configuration

| Parameter                         | Description                                                        | Default               |
| --------------------------------- | ------------------------------------------------------------------ | --------------------- |
| `replicaCount`                    | Replica count                                                      | `1`                   |
| `image.registry`                  | Image registry. You can define private proxy registry              | `docker.io`           |
| `image.repository`                | Image repository in the a registry.                                | `jetbrains/upsource`  |
| `image.pullPolicy`                | Image pull policy                                                  | `IfNotPresent`        |
| `image.tag`                       | Image tag                                                          | `2019.1.1644`         |
| `imagePullSecrets`                | Image pull secrets                                                 | `[]`                  |
| `nameOverride`                    | Name override                                                      | `""`                  |
| `fullnameOverride`                | Full name override                                                 | `""`                  |
| `serviceAccount.create`           | Service account create                                             | `true`                |
| `serviceAccount.annotations`      | Service account annotations                                        | `{}`                  |
| `serviceAccount.name`             | Service account name                                               | `""`                  |
| `podAnnotations`                  | Pod annotations                                                    | `{}`                  |
| `podSecurityContext`              | Pod security context                                               | `{}`                  |
| `securityContext`                 | Security context                                                   | `{}`                  |
| `service.type`                    | Service type: ClusterIP or NodePort                                | `ClusterIP`           |
| `service.port`                    | Service port                                                       | `80`                  |
| `ingress.enabled`                 | Enables Ingress                                                    | `false`               |
| `ingress.annotations`             | Ingress annotations                                                | `{}`                  |
| `ingress.hosts`                   | Ingress accepted hostnames                                         | `chart-example.local` |
| `ingress.paths`                   | Ingress paths                                                      | `[]`                  |
| `ingress.tls`                     | Ingress TLS configuration                                          | `[]`                  |
| `persistence.enabled`             | Enables persistent storage                                         | `true`                |
| `persistence.accessMode`          | Access mode in storage                                             | `ReadWriteOnce`       |
| `persistence.size`                | Persistent storage size                                            | `8Gi`                 |
| `persistence.annotations`         | Persistence annotations                                            | `{}`                  |
| `persistence.enabled`             | Enables persistent storage                                         | `true`                |
| `resources`                       | Resources limit and request                                        | `{}`                  |
| `NodeSelector`                    | Node selector                                                      | `{}`                  |
| `tolerations`                     | Tolerations                                                        | `[]`                  |
| `affinity`                        | Affinity                                                           | `{}`                  |
