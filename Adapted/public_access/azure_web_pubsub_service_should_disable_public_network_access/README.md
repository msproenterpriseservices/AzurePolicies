# Azure Web PubSub Service should disable public network access

## Display Name

Azure Web PubSub Service should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that Azure Web PubSub service isn't exposed on the public internet. Creating private endpoints can limit exposure of Azure Web PubSub service.

## Built-In Reference

Modified from: [WebPubSub_PublicNetworkAccessDisabled_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Web%20PubSub/WebPubSub_PublicNetworkAccessDisabled_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_web_pubsub_service_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_web_pubsub_service_should_disable_public_network_access"
  display_name          = "Azure Web PubSub Service should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that Azure Web PubSub service isn't exposed on the public internet. Creating private endpoints can limit exposure of Azure Web PubSub service."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
