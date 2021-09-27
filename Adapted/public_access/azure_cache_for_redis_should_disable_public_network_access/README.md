# Azure Cache for Redis should disable public network access

## Display Name

Azure Cache for Redis should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that the Azure Cache for Redis isn't exposed on the public internet. You can limit exposure of your Azure Cache for Redis by creating private endpoints instead.

## Built-In Reference

Modified from: [RedisCache_PublicNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Cache/RedisCache_PublicNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_cache_for_redis_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_cache_for_redis_should_disable_public_network_access"
  display_name          = "Azure Cache for Redis should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the Azure Cache for Redis isn't exposed on the public internet. You can limit exposure of your Azure Cache for Redis by creating private endpoints instead."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
