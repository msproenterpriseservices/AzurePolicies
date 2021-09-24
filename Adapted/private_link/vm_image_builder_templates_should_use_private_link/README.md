# VM Image Builder templates should use private link

## Display Name

VM Image Builder templates should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your VM Image Builder building resources, data leakage risks are reduced.

## Built-In Reference

Modified from: [PrivateLinkEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/VM%20Image%20Builder/PrivateLinkEnabled_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "vm_image_builder_templates_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "vm_image_builder_templates_should_use_private_link"
  display_name          = "VM Image Builder templates should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your VM Image Builder building resources, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
