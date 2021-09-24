# App Service should use private link

## Display Name

App Service should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to App Service, you can reduce data leakage risks.

## Built-In Reference

Modified from: [AppService_PrivateEndpoint_AINE](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/App%20Service/AppService_PrivateEndpoint_AINE.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "app_service_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "app_service_should_use_private_link"
  display_name          = "App Service should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to App Service, you can reduce data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
