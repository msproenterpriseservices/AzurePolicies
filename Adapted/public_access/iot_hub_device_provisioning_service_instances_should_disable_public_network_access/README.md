# IoT Hub device provisioning service instances should disable public network access

## Display Name

IoT Hub device provisioning service instances should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that IoT Hub device provisioning service instance isn't exposed on the public internet. Creating private endpoints can limit exposure of the IoT Hub device provisioning instances.

## Built-In Reference

Modified from: [IoTDps_DisablePublicNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Internet%20of%20Things/IoTDps_DisablePublicNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "iot_hub_device_provisioning_service_instances_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "iot_hub_device_provisioning_service_instances_should_disable_public_network_access"
  display_name          = "IoT Hub device provisioning service instances should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that IoT Hub device provisioning service instance isn't exposed on the public internet. Creating private endpoints can limit exposure of the IoT Hub device provisioning instances."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
