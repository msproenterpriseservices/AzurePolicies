# App Services should disable public network access

## Display Name

App Services should disable public network access

## Mode

`Indexed`

## Description

Disabling public network access improves security by ensuring that the App Service is not exposed on the public internet. Creating private endpoints can limit exposure of an App Service.

## Built-In Reference

Modified from: [AppService_PublicNetworkAccess_AINE](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/App%20Service/AppService_PublicNetworkAccess_AINE.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "app_services_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "app_services_should_disable_public_network_access"
  display_name          = "App Services should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the App Service is not exposed on the public internet. Creating private endpoints can limit exposure of an App Service."
  policy_category       = "PublicAccess"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
