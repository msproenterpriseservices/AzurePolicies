# Public network access should be disabled for PostgreSQL servers

## Display Name

Public network access should be disabled for PostgreSQL servers

## Mode

`Indexed`

## Description

Disable the public network access property to improve security and ensure your Azure Database for PostgreSQL can only be accessed from a private endpoint. This configuration disables access from any public address space outside of Azure IP range, and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [PostgreSQL_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/PostgreSQL_DisablePublicNetworkAccess_Audit.json)
