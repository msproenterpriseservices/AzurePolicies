# Azure API for FHIR should use private link

## Display Name

Azure API for FHIR should use private link

## Mode

`Indexed`

## Description

Azure API for FHIR should have at least one approved private endpoint connection. Clients in a virtual network can securely access resources that have private endpoint connections through private links.

## Built-In Reference

Modified from: [HealthcareAPIs_PrivateLink_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/API%20for%20FHIR/HealthcareAPIs_PrivateLink_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_api_for_fhir_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_api_for_fhir_should_use_private_link"
  display_name          = "Azure API for FHIR should use private link"
  policy_description    = "Azure API for FHIR should have at least one approved private endpoint connection. Clients in a virtual network can securely access resources that have private endpoint connections through private links."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
