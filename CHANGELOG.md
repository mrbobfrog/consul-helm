## UNRELEASED

IMPROVEMENTS:

  * RBAC support for `syncCatalog`. This is enabled by default if the catalog
    sync is enabled but can be controlled with `syncCatalog.rbac.enabled`.
    This will create the `ClusterRole` and `ClusterRoleBinding` necessary
    for the catalog sync. [GH-29]
  * client: agents now have the node name set to the actual K8S node name [GH-14]
  * RBAC support for `connectInject`. This will create a `ClusterRole`, `ClusterRoleBinding`,
    and `ServiceAccount` that is necessary for the connect injector to automatically generate
    TLS certificates to interact with the Kubernetes API.

BUG FIXES:

  * Updated images to point to latest versions for 0.3.0.
  * Add missing continuation characters to long commands [GH-26].
  * connectInject: set the correct namespace for the MutatingWebhookConfiguration
    so that deployments work in non-default namespaces. [GH-41]

## 0.3.0 (October 11, 2018)

FEATURES:

  * `connectInject` can install the automatic Connect sidecar injector.

## 0.2.0 (September 26, 2018)

FEATURES:

  * `syncCatalog` can install the [service catalog sync](https://www.hashicorp.com/blog/consul-and-kubernetes-service-catalog-sync)
    functionality.

IMPROVEMENTS:

  * server: support `storageClass` [GH-7]

## 0.1.0

Initial release
