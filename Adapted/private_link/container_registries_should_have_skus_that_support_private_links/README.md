# Container registries should have SKUs that support Private Links

## Display Name

Container registries should have SKUs that support Private Links

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your container registries instead of the entire service, data leakage risks are reduced.

## Built-In Reference

Modified from: [ACR_SkuSupportsPrivateEndpoints_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_SkuSupportsPrivateEndpoints_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "container_registries_should_have_skus_that_support_private_links" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "container_registries_should_have_skus_that_support_private_links"
  display_name          = "Container registries should have SKUs that support Private Links"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your container registries instead of the entire service, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```
