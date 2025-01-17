# Conjur Azure DevOps Extension
Azure Devops Task Extension for retrieving secrets from the CyberArk Conjur Secrets Manager

[Get it on the Azure Marketplace](https://marketplace.visualstudio.com/items?itemName=InfamousJoeG.cyberark-conjur-secrets)

## Requirements
- Conjur Secrets Manager Enterprise v10+
- Conjur Secrets Manager Open Source v1.1+
- Azure DevOps

## Usage

For the full demonstration repository, please visit [https://github.com/infamousjoeg/azure-devops-demo](https://github.com/infamousjoeg/azure-devops-demo).

### Declaring GetConjurSecret Task

```yaml
- task: GetConjurSecret@1
  inputs:
    conjurApplianceURL: 'https://conjur.example.com'
    conjurAccount: 'demo'
    conjurUsername: 'host/cloud/azure/devops/pipeline-demo'
    conjurAPIKey: $(API_KEY)
    ignoreSSL: false
```

## Development

Please follow this guide to properly set up this extension:
https://docs.microsoft.com/en-us/azure/devops/extend/develop/add-build-task?view=azure-devops

## Contributing
We welcome contributions of all kinds to this repository. For instructions on how to get started and descriptions
of our development workflows, please see our [contributing guide](CONTRIBUTING.md).

## License
This repository is licensed under Apache License 2.0 - see [`LICENSE`](LICENSE) for more details.
