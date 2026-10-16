# India DevOps GitOps

GitOps repository for the India Web application.

## Structure

- `apps/india-web/`: Helm chart for the application.
- `argocd/`: Argo CD Application definitions.

## Deployment workflow

1. Jenkins builds and tests the application.
2. Jenkins publishes a versioned Docker image.
3. The GitOps repository records the desired image tag.
4. Argo CD detects Git changes and synchronizes Kubernetes.
5. Kubernetes maintains the desired application state.
