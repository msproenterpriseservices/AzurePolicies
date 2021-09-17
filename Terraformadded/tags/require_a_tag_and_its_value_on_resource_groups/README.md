# Require a tag and its value on resource groups

## Display Name

Require a tag and its value on resource groups

## Mode

`All`

## Description

Enforces a required tag and its value on resource groups.

## Built-In Reference

Modified from: [ResourceGroupRequireTagAndValue_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupRequireTagAndValue_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "require_a_tag_and_its_value_on_resource_groups" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "require_a_tag_and_its_value_on_resource_groups"
  display_name          = "Require a tag and its value on resource groups"
  policy_description    = "Enforces a required tag and its value on resource groups."
  policy_category       = "Tags"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
