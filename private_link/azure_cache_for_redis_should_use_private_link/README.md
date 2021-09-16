# Azure Cache for Redis should use private link

## Display Name

Azure Cache for Redis should use private link

## Mode

`Indexed`

## Description

Private endpoints lets you connect your virtual network to Azure services without a public IP address at the source or destination. By mapping private endpoints to your Azure Cache for Redis instances, data leakage risks are reduced.

## Built-In Reference

Modified from: [RedisCache_PrivateEndpoint_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Cache/RedisCache_PrivateEndpoint_AuditIfNotExists.json)