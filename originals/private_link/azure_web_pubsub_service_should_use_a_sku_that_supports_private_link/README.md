# Azure Web PubSub Service should use a SKU that supports private link

## Display Name

Azure Web PubSub Service should use a SKU that supports private link

## Mode

`Indexed`

## Description

With supported SKU, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Web PubSub service, you can reduce data leakage risks.

## Built-In Reference

Modified from: [WebPubSub_AllowedSKU_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Web%20PubSub/WebPubSub_AllowedSKU_AuditDeny.json)