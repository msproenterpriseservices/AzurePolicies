# Azure Cognitive Search service should use a SKU that supports private link

## Display Name

Azure Cognitive Search service should use a SKU that supports private link

## Mode

`Indexed`

## Description

With supported SKUs of Azure Cognitive Search, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Search service, data leakage risks are reduced.

## Built-In Reference

Modified from: [Search_RequirePrivateLinkSupportedResource_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Search/Search_RequirePrivateLinkSupportedResource_Deny.json)