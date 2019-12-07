### Client credentials in keycloak


[openid connect - Keycloak Client Credentials Flow Clarification - Stack Overflow](https://stackoverflow.com/questions/41756879/keycloak-client-credentials-flow-clarification)




```shell
I think you're misunderstanding some Oauth concepts right here. The client_credentials grant should only be used for a service itself to grant access to an specific resource. Imagine this scenario:

End User -> Docs Service -> Docs Repo

The end user has access to some docs stored in the repo through the docs service. In this case, the service makes the decision to grant the user access to a specific document or not, since the repo is a mere content server. Obviously, both of them are secured through two different keycloak clients.

However, the docs service needs to have full access to the repo. He can access any document he requests. The solution is to give the docs service a service account role, let's say DOC_MANAGER and make the repo check for this role when a resource is requested. The service authenticates with client_credentials and gets access to the resource as a service.

But the end user will perform a standard login, using the Authorization code flow, for example, and get access to the doc through the service. The service will check for another role, let's say DOC_USER and check whether the user has access to this concrete resource or not, before going to the repo.

You can read more about keycloak service accounts here.
```
