# Container registries should have SKUs that support Private Links

## Display Name

Container registries should have SKUs that support Private Links
## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your container registries instead of the entire service, data leakage risks are reduced.

## Built-In Reference

Modified from: [ACR_SkuSupportsPrivateEndpoints_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_SkuSupportsPrivateEndpoints_AuditDeny.json)