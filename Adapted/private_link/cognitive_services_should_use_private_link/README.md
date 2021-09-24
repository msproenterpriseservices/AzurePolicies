# Cognitive Services should use private link

## Display Name

Cognitive Services should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Cognitive Services, you'll reduce the potential for data leakage.

## Built-In Reference

Modified from: [CognitiveServices_EnablePrivateEndpoints_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Cognitive%20Services/CognitiveServices_EnablePrivateEndpoints_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "cognitive_services_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "cognitive_services_should_use_private_link"
  display_name          = "Cognitive Services should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Cognitive Services, you'll reduce the potential for data leakage."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
