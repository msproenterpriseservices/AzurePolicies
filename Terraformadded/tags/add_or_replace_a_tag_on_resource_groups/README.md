# Add or replace a tag on resource groups

## Display Name

Add or replace a tag on resource groups

## Mode

`All`

## Description

Adds or replaces the specified tag and value when any resource group is created or updated. Existing resource groups can be remediated by triggering a remediation task.

## Built-In Reference

Modified from: [AddOrReplaceTag_ResourceGroup_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddOrReplaceTag_ResourceGroup_Modify.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "add_or_replace_a_tag_on_resource_groups" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "add_or_replace_a_tag_on_resource_groups"
  display_name          = "Add or replace a tag on resource groups"
  policy_description    = "Adds or replaces the specified tag and value when any resource group is created or updated. Existing resource groups can be remediated by triggering a remediation task."
  policy_category       = "Tags"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
