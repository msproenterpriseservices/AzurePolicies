# Public network access should be disabled for Azure File Sync

## Display Name

Public network access should be disabled for Azure File Sync

## Mode

`Indexed`

## Description

Disabling the public endpoint allows you to restrict access to your Storage Sync Service resource to requests destined to approved private endpoints on your organization's network. There is nothing inherently insecure about allowing requests to the public endpoint, however, you may wish to disable it to meet regulatory, legal, or organizational policy requirements. You can disable the public endpoint for a Storage Sync Service by setting the incomingTrafficPolicy of the resource to AllowVirtualNetworksOnly.

## Built-In Reference

Modified from: [StorageSync_IncomingTrafficPolicy_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Storage/StorageSync_IncomingTrafficPolicy_AuditDeny.json)
