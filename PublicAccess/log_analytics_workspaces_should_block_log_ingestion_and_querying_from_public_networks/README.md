# Log Analytics workspaces should block log ingestion and querying from public networks

## Display Name

Log Analytics workspaces should block log ingestion and querying from public networks

## Mode

`All`

## Description

Improve workspace security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs on this workspace.

## Built-In Reference

Modified from: [LogAnalyticsWorkspaces_NetworkAccessEnabled_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Monitoring/LogAnalyticsWorkspaces_NetworkAccessEnabled_Deny.json)