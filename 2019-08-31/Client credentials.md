### Client credentials


[Access Keycloak REST Admin API using a service account (client credential grant) - Stack Overflow](https://stackoverflow.com/questions/52238839/access-keycloak-rest-admin-api-using-a-service-account-client-credential-grant)




```shell
Keycloak differentiates between the Scopes/Scope mapping & the roles management.

The Scopes tab: you see in the question above only manages the roles that a client is allowed to request.

For the client credential grant to work these roles must be assigned to the client in the "Service Account Roles" Tab.

So in the end the client receive a token that is the intersection of both of those configurations.

Source: https://www.keycloak.org/docs/latest/server_admin/index.html#_service_accounts
```
