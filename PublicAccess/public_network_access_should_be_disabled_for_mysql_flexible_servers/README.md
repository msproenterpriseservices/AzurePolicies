# Public network access should be disabled for MySQL flexible servers

## Display Name

Public network access should be disabled for MySQL flexible servers

## Mode

`Indexed`

## Description

Disabling the public network access property improves security by ensuring your Azure Database for MySQL flexible servers can only be accessed from a private endpoint. This configuration strictly disables access from any public address space outside of Azure IP range and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [MySQL_FlexibleServers_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MySQL_FlexibleServers_DisablePublicNetworkAccess_Audit.json)
