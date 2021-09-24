# Azure Media Services should use private link

## Display Name

Azure Media Services should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Media Services, you can reduce data leakage risks.

## Built-In Reference

Modified from: [MediaServices_PrivateLink_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Media%20Services/MediaServices_PrivateLink_AuditIfNotExists.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_media_services_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_media_services_should_use_private_link"
  display_name          = "Azure Media Services should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Media Services, you can reduce data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
