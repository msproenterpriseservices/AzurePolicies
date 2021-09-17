# VM Image Builder templates should use private link

## Display Name

VM Image Builder templates should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your VM Image Builder building resources, data leakage risks are reduced.

## Built-In Reference

Modified from: [PrivateLinkEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/VM%20Image%20Builder/PrivateLinkEnabled_Audit.json)