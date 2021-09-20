# App Configuration should use a SKU that supports private link

## Display Name

App Configuration should use a SKU that supports private link

## Mode

`Indexed`

## Description

When using a supported SKU, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your app configuration instances instead of the entire service, you'll also be protected against data leakage risks.

## Built-In Reference

Modified from: [PrivateLink_AllowedSku_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/App%20Configuration/PrivateLink_AllowedSku_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "app_configuration_should_use_a_sku_that_supports_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "app_configuration_should_use_a_sku_that_supports_private_link"
  display_name          = "App Configuration should use a SKU that supports private link"
  policy_description    = "When using a supported SKU, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your app configuration instances instead of the entire service, you'll also be protected against data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
