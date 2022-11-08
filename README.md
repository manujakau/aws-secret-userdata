## aws-secret-userdata
Use aws secret manager to store sensitive user-data inputs.

![aws-secret-manager](https://user-images.githubusercontent.com/44127516/200485319-6d3d3cd3-b2d1-4505-9149-607d469786a8.jpg)

Below deployment will create the demo environment that able to fetch secrets from secrets-manager on fly during instances provisioning using userdata. Secrets are only be access by EC2 instances that attached with instances profile which allow to read aws secret manager. Automatic secret rotation been enabled to rotate secret via invoking lambda.

### Cloudformation deployment

- Clone the Repository
- Update the key-pair name parameter in compute.yaml
- Default region is set to use as us-east-1. Therefor change the ami-id if deploy on other regions
- Use "deploy" command-line tool to deploy each stack.
- Start stack deployment with infra, then secrets and finally compute.

```
./deploy [preferred-stack-name-here] [stack-to-deploy(infra/secrets/compute)] [stack-action(create/update)]

ex: ./deploy report-env infra create
    ./deploy report-infra secrets create
    ./deploy report-infra compute create
```