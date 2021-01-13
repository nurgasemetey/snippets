###  graphql initialization client


[apollo-cache-inmemory - npm](https://www.npmjs.com/package/apollo-cache-inmemory "apollo-cache-inmemory - npm")



[javascript - &quot;export 'createNetworkInterface' was not found in 'apollo-client' - Stack Overflow](https://stackoverflow.com/questions/46965564/export-createnetworkinterface-was-not-found-in-apollo-client "javascript - &quot;export 'createNetworkInterface' was not found in 'apollo-client' - Stack Overflow")



[Token authentication with React and Apollo Client— a custom hook example | by Antoine Sauvage | OVRSEA | Medium](https://medium.com/ovrsea/token-authentication-with-react-and-apollo-client-a-detailed-example-a3cc23760e9 "Token authentication with React and Apollo Client— a custom hook example | by Antoine Sauvage | OVRSEA | Medium")



[Why Apollo Client? - Client (React) - Apollo GraphQL Docs](https://www.apollographql.com/docs/react/why-apollo/ "Why Apollo Client? - Client (React) - Apollo GraphQL Docs")


 

```
const httpLink = new HttpLink({
  uri: 'https://api.github.com/graphql',
});

// Global.Apollo
const authMiddleware = (authToken) =>
  new ApolloLink((operation, forward) => {
    // add the authorization to the headers
    if (authToken) {
      operation.setContext({
        headers: {
          authorization: `Bearer ${authToken}`,
        },
      });
    }

    return forward(operation);
  });
// export const useAppApolloClient = () => {
//   const authToken = '2b46981edd1fef0c84eaad54e7f86650f58e2446';
//   return new ApolloClient({
//     link: authMiddleware(authToken).concat(httpLink),
//   });
// };
const client = new ApolloClient({
  cache: new InMemoryCache(),
  link: authMiddleware('2b46981edd1fef0c84eaad54e7f86650f58e2446').concat(httpLink),
});
```
