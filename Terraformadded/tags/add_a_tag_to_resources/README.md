# Add a tag to resources

## Display Name

Add a tag to resources

## Mode

`Indexed`

## Description

Adds the specified tag and value when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed. Does not modify tags on resource groups.

## Built-In Reference

Modified from: [AddTag_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/AddTag_Modify.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "add_a_tag_to_resources" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "add_a_tag_to_resources"
  display_name          = "Add a tag to resources"
  policy_description    = "Adds the specified tag and value when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed. Does not modify tags on resource groups."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
