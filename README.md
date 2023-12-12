



## Helm Chart Customization for Keycloak
This repository contains the Helm chart customization for deploying Keycloak in a Kubernetes cluster.

## Instructions
For detailed instructions and configuration guidelines, please refer to the [Keycloak Documentation](Keycloak_Deployment.pdf)

Updates:
- Pulled the bitnami/keycloak helm chart and customised default templates:
- Updated statefulset.yaml template to add CLIENT_ROOT_URL variable if clientRootUrl is set in values.yaml
- Added an extra-secret.yaml template to create a secret from the realm.json file if clientRootUrl is set in values.yaml
- Added realm.json file with ${CLIENT_ROOT_URL} placeholder
- Updated the following values in test-values.yaml: clientRootUrl, extraVolumes, extraVolumeMounts and extraEnv.
