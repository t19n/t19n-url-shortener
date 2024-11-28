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

### Create user for GH Actions

```bash
az ad sp create-for-rbac --name "Github-Actions-SP" \
                         --role contributor \
                         --scope /subscriptions/SUBSCRIPTION_ID \
                         --sdk-auth
```
