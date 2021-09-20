# Azure Monitor Private Link Scope should use private link

## Display Name

Azure Monitor Private Link Scope should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Monitor Private Links Scope, you can reduce data leakage risks.

## Built-In Reference

Modified from: [AzureMonitorPrivateLinkScopes_PrivateEndpoints_AINE](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Monitoring/AzureMonitorPrivateLinkScopes_PrivateEndpoints_AINE.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_monitor_private_link_scope_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_monitor_private_link_scope_should_use_private_link"
  display_name          = "Azure Monitor Private Link Scope should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Monitor Private Links Scope, you can reduce data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
