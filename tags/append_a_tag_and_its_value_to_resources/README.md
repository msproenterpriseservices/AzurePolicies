# Append a tag and its value to resources

## Display Name

Append a tag and its value to resources

## Mode

`Indexed`

## Description

Appends the specified tag and value when any resource which is missing this tag is created or updated. Does not modify the tags of resources created before this policy was applied until those resources are changed. Does not apply to resource groups. New 'modify' effect policies are available that support remediation of tags on existing resources (see https://aka.ms/modifydoc).

## Built-In Reference

Modified from: [ApplyTag_Append](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ApplyTag_Append.json)