# Log Analytics workspaces should block log ingestion and querying from public networks

## Display Name

Log Analytics workspaces should block log ingestion and querying from public networks

## Mode

`All`

## Description

Improve workspace security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs on this workspace.

## Built-In Reference

Modified from: [LogAnalyticsWorkspaces_NetworkAccessEnabled_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Monitoring/LogAnalyticsWorkspaces_NetworkAccessEnabled_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "log_analytics_workspaces_should_block_log_ingestion_and_querying_from_public_networks" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "log_analytics_workspaces_should_block_log_ingestion_and_querying_from_public_networks"
  display_name          = "Log Analytics workspaces should block log ingestion and querying from public networks"
  policy_description    = "Improve workspace security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs on this workspace."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
