# Require a tag on resources

## Display Name

Require a tag on resources

## Mode

`Indexed`

## Description

Enforces existence of a tag. Does not apply to resource groups.

## Built-In Reference

Modified from: [RequireTag_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/RequireTag_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "require_a_tag_on_resources" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "require_a_tag_on_resources"
  display_name          = "Require a tag on resources"
  policy_description    = "Enforces existence of a tag. Does not apply to resource groups."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
