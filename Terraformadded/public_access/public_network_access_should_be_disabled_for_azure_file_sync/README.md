# Public network access should be disabled for Azure File Sync

## Display Name

Public network access should be disabled for Azure File Sync

## Mode

`All`

## Description

Disabling the public endpoint allows you to restrict access to your Storage Sync Service resource to requests destined to approved private endpoints on your organization's network. There is nothing inherently insecure about allowing requests to the public endpoint, however, you may wish to disable it to meet regulatory, legal, or organizational policy requirements. You can disable the public endpoint for a Storage Sync Service by setting the incomingTrafficPolicy of the resource to AllowVirtualNetworksOnly.

## Built-In Reference

Modified from: [StorageSync_IncomingTrafficPolicy_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Storage/StorageSync_IncomingTrafficPolicy_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_should_be_disabled_for_azure_file_sync" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_should_be_disabled_for_azure_file_sync"
  display_name          = "Public network access should be disabled for Azure File Sync"
  policy_description    = "Disabling the public endpoint allows you to restrict access to your Storage Sync Service resource to requests destined to approved private endpoints on your organization's network. There is nothing inherently insecure about allowing requests to the public endpoint, however, you may wish to disable it to meet regulatory, legal, or organizational policy requirements. You can disable the public endpoint for a Storage Sync Service by setting the incomingTrafficPolicy of the resource to AllowVirtualNetworksOnly."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
