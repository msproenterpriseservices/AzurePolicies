# Azure File Sync should use private link

## Display Name

Azure File Sync should use private link

## Mode

`Indexed`

## Description

Creating a private endpoint for the indicated Storage Sync Service resource allows you to address your Storage Sync Service resource from within the private IP address space of your organization's network, rather than through the internet-accessible public endpoint. Creating a private endpoint by itself does not disable the public endpoint.

## Built-In Reference

Modified from: [StorageSync_PrivateEndpoint_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Storage/StorageSync_PrivateEndpoint_AuditIfNotExists.json)