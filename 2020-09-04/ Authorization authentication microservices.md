###  Authorization authentication microservices





 

```
auth with microservices
Authorization and Authentication are hard. when you only have to implement them once (as you do within a monolith) instead of over and over again, it makes the developer happy :-), and maybe leads to less implementation failures.

When you have a bunch of microservices, this is something that has to be considered.

Implement it once or in every microservice, or something in between?

approach 1
do authentication and authorization in every microservice
pros

makes developer happy :)
less implementation errors
less risk of forgetting to handle at all
centrally defined and handled
smaller micro services
less repetition in the code in the micro services
cons

service can not have fine grained object permissions
all or nothing authorization
global auth bottleneck
approach 2
do authentication globally, and authorization in every microservice
pros

global authentication is easier to manage/control
fine grained object permissions are possible
cons

slightly more code in the micro services
needs some effort to have an overview what you can do with which permission
approach 3
do authentication in every microservice, and authorization globally
is listed only for completeness. it does not make sense -> worst of both worlds.

no fine grained object permissions and error prone and tedious repetitive authentication

approach 3
do authentication and authorization in every microservice
pros

fine grained object permissions are possible
different user authentication mechanisms are possible for different microservices
cons

error prone
many repetitions
bigger micro services
needs some effort to have an overview what you can do with which permission
no happy developer :-(
links
https://blog.andyet.com/2015/05/12/micro-services-user-info-and-auth
http://nordicapis.com/how-to-control-user-identity-within-microservices/
https://www.appsflyer.com/blog/how-we-solved-authentication-and-authorization-in-our-microservices-architecture/
http://microservices.io/patterns/apigateway.html
```
