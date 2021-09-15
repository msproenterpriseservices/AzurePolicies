# Public network access on Azure SQL Database should be disabled

## Display Name

Public network access on Azure SQL Database should be disabled

## Mode

`All`

## Description

Disabling the public network access property improves security by ensuring your Azure SQL Database can only be accessed from a private endpoint. This configuration denies all logins that match IP or virtual network based firewall rules.

## Built-In Reference

Modified from: [SqlServer_PublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/SqlServer_PublicNetworkAccess_Audit.json)