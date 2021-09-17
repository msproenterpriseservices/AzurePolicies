# Inherit a tag from the resource group if missing

## Display Name

Inherit a tag from the resource group if missing

## Mode

`Indexed`

## Description

Adds the specified tag with its value from the parent resource group when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed.

## Built-In Reference

Modified from: [InheritTag_Add_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Add_Modify.json)


Terraform azpolicy_definition module usage
-----

```hcl
module "inherit_a_tag_from_the_resource_group_if_missing" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "inherit_a_tag_from_the_resource_group_if_missing"
  display_name          = "Inherit a tag from the resource group if missing"
  policy_description    = "Adds the specified tag with its value from the parent resource group when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
