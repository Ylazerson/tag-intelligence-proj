# B"H



## Ensure `~/.dbt/profiles.yml` has correct entry for pde:

```sh
cat ~/.dbt/profiles.yml
```


```yml
    pde:
      type: snowflake
      account: psb24919.us-east-1
      user: izzy.lazerson
      private_key_path: /home/izzy/.pointfive/snowflake-pde-rsa-key.p8
      database: izzy_lazerson
      warehouse: COMPUTE_WH
      schema: public
      threads: 4
      client_session_keep_alive: False
      role: ACCOUNTADMIN
      private_key_passphrase: ''
```



## Smoketest Azure CLI to get info on a resource-id



```sh

# Extracted resource-id:
az account set -s 524a4ec0-d5df-45ec-825c-7a4a3aa7dbbd

az resource show --ids "/subscriptions/524a4ec0-d5df-45ec-825c-7a4a3aa7dbbd/resourcegroups/rg-retailanalyticsbw-run/providers/microsoft.compute/virtualmachines/slc9496"

```