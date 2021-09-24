# Azure SignalR Service should use a Private Link enabled SKU

## Display Name

Azure SignalR Service should use a Private Link enabled SKU

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination which protect your resources against public data leakage risks. The policy limits you to Private Link enabled SKUs for Azure SignalR Service.

## Built-In Reference

Modified from: [SignalR_AllowedSKU_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SignalR/SignalR_AllowedSKU_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_signalr_service_should_use_a_private_link_enabled_sku" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_signalr_service_should_use_a_private_link_enabled_sku"
  display_name          = "Azure SignalR Service should use a Private Link enabled SKU"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination which protect your resources against public data leakage risks. The policy limits you to Private Link enabled SKUs for Azure SignalR Service."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
