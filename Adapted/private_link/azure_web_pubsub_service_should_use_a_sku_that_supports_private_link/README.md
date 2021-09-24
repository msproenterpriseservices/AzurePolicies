# Azure Web PubSub Service should use a SKU that supports private link

## Display Name

Azure Web PubSub Service should use a SKU that supports private link

## Mode

`Indexed`

## Description

With supported SKU, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Web PubSub service, you can reduce data leakage risks.

## Built-In Reference

Modified from: [WebPubSub_AllowedSKU_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Web%20PubSub/WebPubSub_AllowedSKU_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_web_pubsub_service_should_use_a_sku_that_supports_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_web_pubsub_service_should_use_a_sku_that_supports_private_link"
  display_name          = "Azure Web PubSub Service should use a SKU that supports private link"
  policy_description    = "With supported SKU, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Web PubSub service, you can reduce data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
