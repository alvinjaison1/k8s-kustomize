# k8s-kustomize

Directory structure

Application Name:

|-- base
|   |-- deployment.yaml
|   |-- kustomization.yaml
|   `-- service.yaml
`-- overlays
    |-- dev
    |   |-- deployment_patch.yaml
    |   |-- ingress.yaml
    |   `-- kustomization.yaml
    |-- prod
    |   |-- deployment_patch.yaml
    |   |-- ingress.yaml
    |   `-- kustomization.yaml
    |-- qa
    |   |-- deployment_patch.yaml
    |   |-- ingress.yaml
    |   `-- kustomization.yaml
    `-- staging
        |-- deployment_patch.yaml
        |-- ingress.yaml
        `-- kustomization.yaml


To apply the above configuration in staging, run the below command in staging bastion host

# kubectl apply -k overlays/staging/
