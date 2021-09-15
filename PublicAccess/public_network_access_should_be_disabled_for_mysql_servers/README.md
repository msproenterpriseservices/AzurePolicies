# Public network access should be disabled for MySQL servers

## Display Name

Public network access should be disabled for MySQL servers

## Mode

`All`

## Description

Disable the public network access property to improve security and ensure your Azure Database for MySQL can only be accessed from a private endpoint. This configuration strictly disables access from any public address space outside of Azure IP range, and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [MySQL_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MySQL_DisablePublicNetworkAccess_Audit.json)