# Append a tag and its value to resource groups

## Display Name

Append a tag and its value to resource groups

## Mode

`All`

## Description

Appends the specified tag and value when any resource group which is missing this tag is created or updated. Does not modify the tags of resource groups created before this policy was applied until those resource groups are changed. New 'modify' effect policies are available that support remediation of tags on existing resources (see https://aka.ms/modifydoc).

## Built-In Reference

Modified from: [ResourceGroupApplyTag_Append](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/ResourceGroupApplyTag_Append.json)