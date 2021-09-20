# App Service apps should use a SKU that supports private link

## Display Name

App Service apps should use a SKU that supports private link

## Mode

`Indexed`

## Description

With supported SKUs, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to apps, you can reduce data leakage risks.

## Built-In Reference

Modified from: [AppService_DisablePrivateEndpoint_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/App%20Service/AppService_DisablePrivateEndpoint_Deny.json.json)