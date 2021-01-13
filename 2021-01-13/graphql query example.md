### graphql query example







```
const GetRepositoryInfoQuery = gql`
{
  viewer {
    starredRepositories(first: 100) {
      edges {
        starredAt
        node {
          name
          description,
          repositoryTopics(first: 100) {
            edges {
              node {
                id
                topic {
                  id
                  name
                }
              }
            }
          }
        }
      }
    }
  }
}
`;

---
const result = await client
          .query({
            query: GetRepositoryInfoQuery
          });
```
