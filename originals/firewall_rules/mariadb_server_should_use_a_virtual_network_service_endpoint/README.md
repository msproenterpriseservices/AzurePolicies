# MariaDB server should use a virtual network service endpoint

## Display Name

MariaDB server should use a virtual network service endpoint

## Mode

`Indexed`

## Description

Virtual network based firewall rules are used to enable traffic from a specific subnet to Azure Database for MariaDB while ensuring the traffic stays within the Azure boundary. This policy provides a way to audit if the Azure Database for MariaDB has virtual network service endpoint being used.

## Built-In Reference

Modified from: [MariaDB_VirtualNetworkServiceEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MariaDB_VirtualNetworkServiceEndpoint_Audit.json)