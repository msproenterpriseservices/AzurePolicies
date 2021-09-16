# Azure Attestation providers should use private endpoints

## Display Name

Azure Attestation providers should use private endpoints

## Mode

`Indexed`

## Description

Private endpoints provide a way to connect Azure Attestation providers to your Azure resources without sending traffic over the public internet. By preventing public access, private endpoints help protect against undesired anonymous access.

## Built-In Reference

Modified from: [Attestation_PrivateLink_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Attestation/Attestation_PrivateLink_AuditIfNotExists.json)