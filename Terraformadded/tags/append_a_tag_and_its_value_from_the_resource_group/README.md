# Append a tag and its value from the resource group

## Display Name

Append a tag and its value from the resource group

## Mode

`Indexed`

## Description

Appends the specified tag with its value from the resource group when any resource which is missing this tag is created or updated. Does not modify the tags of resources created before this policy was applied until those resources are changed. New 'modify' effect policies are available that support remediation of tags on existing resources (see https://aka.ms/modifydoc).

## Built-In Reference

Modified from: [InheritTag_Append](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Append.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "append_a_tag_and_its_value_from_the_resource_group" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "append_a_tag_and_its_value_from_the_resource_group"
  display_name          = "Append a tag and its value from the resource group"
  policy_description    = "Appends the specified tag with its value from the resource group when any resource which is missing this tag is created or updated. Does not modify the tags of resources created before this policy was applied until those resources are changed. New 'modify' effect policies are available that support remediation of tags on existing resources (see https://aka.ms/modifydoc)."
  policy_category       = "Tags"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
