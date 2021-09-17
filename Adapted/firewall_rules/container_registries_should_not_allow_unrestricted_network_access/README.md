# Container registries should not allow unrestricted network access

## Display Name

Container registries should not allow unrestricted network access

## Mode

`Indexed`

## Description

Azure container registries by default accept connections over the internet from hosts on any network. To protect your registries from potential threats, allow access from only specific public IP addresses or address ranges. If your registry doesn't have an IP/firewall rule or a configured virtual network, it will appear in the unhealthy resources.

## Built-In Reference

Modified from: [ACR_NetworkRulesExist_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_NetworkRulesExist_AuditDeny.json)