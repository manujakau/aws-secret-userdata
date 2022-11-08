## aws-secret-userdata
Use aws secret manager to store sensitive user-data inputs.

### Cloudformation deployment

- Clone the Repository
- Update the key-pair name parameter in compute.yaml
- Use "deploy" commandline to deploy each stack.
- Start stack deployment with infra, then secrets and finally compute.

```
./deploy [preferred-stack-name-here] [stack-to-deploy(infra/secrets/compute)] [stack-action(create/update)]

ex: ./deploy report-env infra create
    ./deploy report-infra secrets create
    ./deploy report-infra compute create
```