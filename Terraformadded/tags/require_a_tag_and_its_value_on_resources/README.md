# Require a tag and its value on resources

## Display Name

Require a tag and its value on resources

## Mode

`Indexed`

## Description

Enforces a required tag and its value. Does not apply to resource groups.

## Built-In Reference

Modified from: [RequireTagAndValue_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/RequireTagAndValue_Deny.json)


Terraform azpolicy_definition module usage
-----

```hcl
module "require_a_tag_and_its_value_on_resources" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "require_a_tag_and_its_value_on_resources"
  display_name          = "Require a tag and its value on resources"
  policy_description    = "Enforces a required tag and its value. Does not apply to resource groups."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
