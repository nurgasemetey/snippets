###  cors on nginx


[cors - How do I add Access-Control-Allow-Origin in NGINX? - Server Fault](https://serverfault.com/questions/162429/how-do-i-add-access-control-allow-origin-in-nginx "cors - How do I add Access-Control-Allow-Origin in NGINX? - Server Fault")


 

```conf
server {
  listen        80;
  server_name   api.test.com;


  location / {

    # Simple requests
    if ($request_method ~* "(GET|POST)") {
      add_header "Access-Control-Allow-Origin"  *;
    }

    # Preflighted requests
    if ($request_method = OPTIONS ) {
      add_header "Access-Control-Allow-Origin"  *;
      add_header "Access-Control-Allow-Methods" "GET, POST, OPTIONS, HEAD";
      add_header "Access-Control-Allow-Headers" "Authorization, Origin, X-Requested-With, Content-Type, Accept";
      return 200;
    }

    ....
    # Handle request
    ....
  }
}
```
