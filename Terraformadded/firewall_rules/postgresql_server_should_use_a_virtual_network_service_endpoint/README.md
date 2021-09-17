# PostgreSQL server should use a virtual network service endpoint

## Display Name

PostgreSQL server should use a virtual network service endpoint

## Mode

`Indexed`

## Description

Virtual network based firewall rules are used to enable traffic from a specific subnet to Azure Database for PostgreSQL while ensuring the traffic stays within the Azure boundary. This policy provides a way to audit if the Azure Database for PostgreSQL has virtual network service endpoint being used.

## Built-In Reference

Modified from: [PostgreSQL_VirtualNetworkServiceEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/PostgreSQL_VirtualNetworkServiceEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "postgresql_server_should_use_a_virtual_network_service_endpoint" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "postgresql_server_should_use_a_virtual_network_service_endpoint"
  display_name          = "PostgreSQL server should use a virtual network service endpoint"
  policy_description    = "Virtual network based firewall rules are used to enable traffic from a specific subnet to Azure Database for PostgreSQL while ensuring the traffic stays within the Azure boundary. This policy provides a way to audit if the Azure Database for PostgreSQL has virtual network service endpoint being used."
  policy_category       = "FirewallRules"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
