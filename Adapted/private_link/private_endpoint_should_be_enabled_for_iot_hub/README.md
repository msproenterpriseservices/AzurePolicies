# Private endpoint should be enabled for IoT Hub

## Display Name

Private endpoint should be enabled for IoT Hub

## Mode

`Indexed`

## Description

Private endpoint connections enforce secure communication by enabling private connectivity to IoT Hub. Configure a private endpoint connection to enable access to traffic coming only from known networks and prevent access from all other IP addresses, including within Azure.

## Built-In Reference

Modified from: [IoTHub_EnablePrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Internet%20of%20Things/IoTHub_EnablePrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "private_endpoint_should_be_enabled_for_iot_hub" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "private_endpoint_should_be_enabled_for_iot_hub"
  display_name          = "Private endpoint should be enabled for IoT Hub"
  policy_description    = "Private endpoint connections enforce secure communication by enabling private connectivity to IoT Hub. Configure a private endpoint connection to enable access to traffic coming only from known networks and prevent access from all other IP addresses, including within Azure."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
