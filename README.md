# Azure resource group and storage account service module

Bicep to deploy a resource group and service account into Azure.

## to call this from a GitHub Action workflow in your repository

```yaml
name: example azure resource group and storage account reusable workflow dispatch

on:
  workflow_dispatch: # Manually triggered by the user in GitHub repo on the Actions tab

jobs:
  deploy-azure-rg-and-st:
    name: deploy a resource group and storage account to azure
    uses: JasonCubic/azure-rg-and-st/.github/workflows/call.yaml@v0.1.1
    with:
      resource-group-name: rg-ga-test
      storage-account-prefix: storage
    secrets:
      tenant-id: ${{ secrets.TENANT_ID }}
      subscription-id: ${{ secrets.SUBSCRIPTION_ID }}
      client-id: ${{ secrets.CLIENT_ID }}
      client-secret: ${{ secrets.CLIENT_SECRET }}
```

## Support

- To use this repo we ask that you make your repo InnerSource.  That way other teams can learn from you, and you can learn from other teams.
- Support is to be done by leaving issues on this repo in the issues tab.  But if the support requires troubleshooting a problem, then you will be asked to share your repository.
- You are invited to send pull requests to modify or add reusable workflows.  Especially if they are something that could be reusable.  Review the contributing.md instructions before sending a pull request.
