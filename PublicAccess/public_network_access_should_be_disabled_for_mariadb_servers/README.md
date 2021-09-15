# Public network access should be disabled for MariaDB servers

## Display Name

Public network access should be disabled for MariaDB servers

## Mode

`All`

## Description

Disable the public network access property to improve security and ensure your Azure Database for MariaDB can only be accessed from a private endpoint. This configuration strictly disables access from any public address space outside of Azure IP range, and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [MariaDB_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MariaDB_DisablePublicNetworkAccess_Audit.json)