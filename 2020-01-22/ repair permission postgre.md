###  repair permission postgre


[Error: Config owner (usuario:1000) and data owner (postgres:116) do not match, and config owner is not root - ZeroGlosa](https://makandracards.com/zeroglosa/29849-error-config-owner-usuario-1000-and-data-owner-postgres-116-do-not-match-and-config-owner-is-not-root "Error: Config owner (usuario:1000) and data owner (postgres:116) do not match, and config owner is not root - ZeroGlosa")


 

```shell
sudo chown postgres:postgres /etc/postgresql/9.3/main/postgresql.conf
```
