# Azure File Sync should use private link

## Display Name

Azure File Sync should use private link

## Mode

`Indexed`

## Description

Creating a private endpoint for the indicated Storage Sync Service resource allows you to address your Storage Sync Service resource from within the private IP address space of your organization's network, rather than through the internet-accessible public endpoint. Creating a private endpoint by itself does not disable the public endpoint.

## Built-In Reference

Modified from: [StorageSync_PrivateEndpoint_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Storage/StorageSync_PrivateEndpoint_AuditIfNotExists.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_file_sync_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_file_sync_should_use_private_link"
  display_name          = "Azure File Sync should use private link"
  policy_description    = "Creating a private endpoint for the indicated Storage Sync Service resource allows you to address your Storage Sync Service resource from within the private IP address space of your organization's network, rather than through the internet-accessible public endpoint. Creating a private endpoint by itself does not disable the public endpoint."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
