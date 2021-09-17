# Add or replace a tag on resources

## Display Name

Add or replace a tag on resources

## Mode

`Indexed`

## Description

Adds or replaces the specified tag and value when any resource is created or updated. Existing resources can be remediated by triggering a remediation task. Does not modify tags on resource groups.

## Built-In Reference

Modified from: [AddOrReplaceTag_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddOrReplaceTag_Modify.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "add_or_replace_a_tag_on_resources" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "add_or_replace_a_tag_on_resources"
  display_name          = "Add or replace a tag on resources"
  policy_description    = "Adds or replaces the specified tag and value when any resource is created or updated. Existing resources can be remediated by triggering a remediation task. Does not modify tags on resource groups."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
