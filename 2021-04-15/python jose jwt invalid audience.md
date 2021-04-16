### python jose jwt invalid audience


[Token decode gives error 'Invalid audience' · Issue #89 · marcospereirampj/python-keycloak](https://github.com/marcospereirampj/python-keycloak/issues/89 "Token decode gives error 'Invalid audience' · Issue #89 · marcospereirampj/python-keycloak")


 

```
options = {"verify_signature": True, "verify_aud": False, "exp": True}
        return keycloak_instance.decode_token(given_token, key=given_key, options=options)

```
