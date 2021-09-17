# IoT Hub device provisioning service instances should use private link

## Display Name

IoT Hub device provisioning service instances should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to the IoT Hub device provisioning service, data leakage risks are reduced.

## Built-In Reference

Modified from: [IoTDps_EnablePrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Internet%20of%20Things/IoTDps_EnablePrivateEndpoint_Audit.json)