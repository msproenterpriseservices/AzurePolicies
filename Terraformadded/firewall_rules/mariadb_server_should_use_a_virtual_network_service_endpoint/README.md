# MariaDB server should use a virtual network service endpoint

## Display Name

MariaDB server should use a virtual network service endpoint

## Mode

`Indexed`

## Description

Virtual network based firewall rules are used to enable traffic from a specific subnet to Azure Database for MariaDB while ensuring the traffic stays within the Azure boundary. This policy provides a way to audit if the Azure Database for MariaDB has virtual network service endpoint being used.

## Built-In Reference

Modified from: [MariaDB_VirtualNetworkServiceEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MariaDB_VirtualNetworkServiceEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "mariadb_server_should_use_a_virtual_network_service_endpoint" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "mariadb_server_should_use_a_virtual_network_service_endpoint"
  display_name          = "MariaDB server should use a virtual network service endpoint"
  policy_description    = "Virtual network based firewall rules are used to enable traffic from a specific subnet to Azure Database for MariaDB while ensuring the traffic stays within the Azure boundary. This policy provides a way to audit if the Azure Database for MariaDB has virtual network service endpoint being used."
  policy_category       = "FirewallRules"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
