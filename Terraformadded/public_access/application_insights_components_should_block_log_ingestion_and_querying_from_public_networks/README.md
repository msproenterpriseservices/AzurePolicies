# Application Insights components should block log ingestion and querying from public networks

## Display Name

Application Insights components should block log ingestion and querying from public networks

## Mode

`All`

## Description

Improve Application Insights security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs of this component.

## Built-In Reference

Modified from: [ApplicationInsightsComponents_NetworkAccessEnabled_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Monitoring/ApplicationInsightsComponents_NetworkAccessEnabled_Deny.json)


Terraform azpolicy_definition module usage
-----

```hcl
module "application_insights_components_should_block_log_ingestion_and_querying_from_public_networks" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "application_insights_components_should_block_log_ingestion_and_querying_from_public_networks"
  display_name          = "Application Insights components should block log ingestion and querying from public networks"
  policy_description    = "Improve Application Insights security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs of this component."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
