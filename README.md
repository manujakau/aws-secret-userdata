## aws-secret-userdata
Use aws secret manager to store sensitive user-data inputs.

![aws-secret-manager](https://user-images.githubusercontent.com/44127516/200485319-6d3d3cd3-b2d1-4505-9149-607d469786a8.jpg)

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