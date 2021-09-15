# Application Insights components should block log ingestion and querying from public networks

## Display Name

Application Insights components should block log ingestion and querying from public networks

## Mode

`Indexed`

## Description

Improve Application Insights security by blocking log ingestion and querying from public networks. Only private-link connected networks will be able to ingest and query logs of this component.

## Built-In Reference

Modified from: [ApplicationInsightsComponents_NetworkAccessEnabled_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Monitoring/ApplicationInsightsComponents_NetworkAccessEnabled_Deny.json)
