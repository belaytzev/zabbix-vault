# Zabbix monitoring for HashiCorp Vault 

## Features
* monitoring health and sealed
* monitoring token expiration time

## Requirements
* curl
* jq

## Macros

* VAULT_URL - full url to Vault (http://localhost:8200)
* VAULT_TOKEN - access token used vault policy

## Vault Policy for Zabbix token

```
path "auth/token/accessors" {
  capabilities = ["list", "sudo"]
}
path "auth/token/lookup-accessor" {
  capabilities = ["update"]
}
```
