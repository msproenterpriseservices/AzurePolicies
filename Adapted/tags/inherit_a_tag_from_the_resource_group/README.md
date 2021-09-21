# Inherit a tag from the resource group

## Display Name

Inherit a tag from the resource group

## Mode

`Indexed`

## Description

Adds or replaces the specified tag and value from the parent resource group when any resource is created or updated. Existing resources can be remediated by triggering a remediation task.

## Built-In Reference

Modified from: [InheritTag_AddOrReplace_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_AddOrReplace_Modify.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "inherit_a_tag_from_the_resource_group" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "inherit_a_tag_from_the_resource_group"
  display_name          = "Inherit a tag from the resource group"
  policy_description    = "Adds or replaces the specified tag and value from the parent resource group when any resource is created or updated. Existing resources can be remediated by triggering a remediation task."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
