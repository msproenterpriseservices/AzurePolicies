# Event Hub namespaces should use private link

## Display Name

Event Hub namespaces should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Event Hub namespaces, data leakage risks are reduced.

## Built-In Reference

Modified from: [EventHub_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Event%20Hub/EventHub_PrivateEndpoint_Audit.json)