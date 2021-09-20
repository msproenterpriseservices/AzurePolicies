# Public network access on Azure IoT Hub should be disabled

## Display Name

Public network access on Azure IoT Hub should be disabled

## Mode

`All`

## Description

Disabling the public network access property improves security by ensuring your Azure IoT Hub can only be accessed from a private endpoint.

## Built-In Reference

Modified from: [IoTHub_DisablePublicNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Internet%20of%20Things/IoTHub_DisablePublicNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_on_azure_iot_hub_should_be_disabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_on_azure_iot_hub_should_be_disabled"
  display_name          = "Public network access on Azure IoT Hub should be disabled"
  policy_description    = "Disabling the public network access property improves security by ensuring your Azure IoT Hub can only be accessed from a private endpoint."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
