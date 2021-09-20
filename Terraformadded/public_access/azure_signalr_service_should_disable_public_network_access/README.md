# Azure SignalR Service should disable public network access

## Display Name

Azure SignalR Service should disable public network access

## Mode

`All`

## Description

To improve the security of Azure SignalR Service resource, ensure that it isn't exposed to the public internet and can only be accessed from a private endpoint. Disable the public network access property as described in https://aka.ms/asrs/networkacls. This option disables access from any public address space outside the Azure IP range, and denies all logins that match IP or virtual network-based firewall rules. This reduces data leakage risks.

## Built-In Reference

Modified from: [SignalR_PublicNetworkAccessDisabled_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SignalR/SignalR_PublicNetworkAccessDisabled_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_signalr_service_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_signalr_service_should_disable_public_network_access"
  display_name          = "Azure SignalR Service should disable public network access"
  policy_description    = "To improve the security of Azure SignalR Service resource, ensure that it isn't exposed to the public internet and can only be accessed from a private endpoint. Disable the public network access property as described in https://aka.ms/asrs/networkacls. This option disables access from any public address space outside the Azure IP range, and denies all logins that match IP or virtual network-based firewall rules. This reduces data leakage risks."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
