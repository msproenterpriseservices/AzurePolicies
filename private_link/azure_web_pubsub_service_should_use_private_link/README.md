# Azure Web PubSub Service should use private link

## Display Name

Azure Web PubSub Service should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Azure Web PubSub Service, you can reduce data leakage risks.

## Built-In Reference

Modified from: [WebPubSub_PrivateEndpointEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Web%20PubSub/WebPubSub_PrivateEndpointEnabled_Audit.json)