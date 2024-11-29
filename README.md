# t19n-url-shortener

Lets Build It: Url Shortener Course

## Infrastructure as Code

### Download Azure CLI

https://learn.microsoft.com/en-us/cli/azure

```bash
az login
```

### Create Resource Group

```bash
az group create --name urlshortener-dev --location westeurope
```

### Deploy Bicep

### What if

```bash
az deployment group what-if --resource-group t19n-urlshortener-dev --template-file infrastructure/main.bicep
```

### Deploy

```bash
az deployment group create --resource-group t19n-urlshortener-dev --template-file infrastructure/main.bicep
```

### Create user for GH Actions

```bash
az ad sp create-for-rbac --name "Github-Actions-SP" \
                         --role contributor \
                         --scope /subscriptions/SUBSCRIPTION_ID \
                         --sdk-auth
```

#### Configure a federated identity credential on an app

https://learn.microsoft.com/en-gb/entra/workload-id/workload-identity-federation-create-trust?pivots=identity-wif-apps-methods-azp#configure-a-federated-identity-credential-on-an-app

## Get Azure Publish Profile

```bash
az webapp deployment list-publishing-profiles --name api-piza2nvlxc5jg --resource-group t19n-urlshortener-dev --xml
```
