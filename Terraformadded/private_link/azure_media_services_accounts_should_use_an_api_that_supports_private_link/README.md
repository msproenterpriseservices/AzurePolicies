# Azure Media Services accounts should use an API that supports Private Link

## Display Name

Azure Media Services accounts should use an API that supports Private Link

## Mode

`Indexed`

## Description

Media Services accounts should be created with an API that supports private link.

## Built-In Reference

Modified from: [MediaServices_RequirePrivateLinkSupport_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Media%20Services/MediaServices_RequirePrivateLinkSupport_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_media_services_accounts_should_use_an_api_that_supports_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_media_services_accounts_should_use_an_api_that_supports_private_link"
  display_name          = "Azure Media Services accounts should use an API that supports Private Link"
  policy_description    = "Media Services accounts should be created with an API that supports private link."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
