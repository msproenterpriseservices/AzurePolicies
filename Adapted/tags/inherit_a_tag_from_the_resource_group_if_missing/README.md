# Inherit a tag from the resource group if missing

## Display Name

Inherit a tag from the resource group if missing

## Mode

`Indexed`

## Description

Adds the specified tag with its value from the parent resource group when any resource missing this tag is created or updated. Existing resources can be remediated by triggering a remediation task. If the tag exists with a different value it will not be changed.

## Built-In Reference

Modified from: [InheritTag_Add_Modify](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Tags/InheritTag_Add_Modify.json)