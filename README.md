# Graph-Ql :

A GraphQL API is an application programming interface that uses GraphQL—a query language developed by Facebook (now Meta)—to interact with data. Unlike traditional REST APIs, which expose fixed endpoints for specific data, GraphQL APIs allow clients to request exactly the data they need in a single request.

## Key Features of GraphQL APIs:
  1. Flexible Data Retrieval:
      - Clients can specify the exact fields they want, reducing over-fetching or under-fetching.
     
  2. Single Endpoint
      - Instead of multiple endpoints (like REST), GraphQL typically uses one endpoint for all operations (e.g., /graphql).
     
  4. Strongly Typed Schema
  
      - The API is defined by a schema that outlines the structure of available queries, mutations, and data types.
    
  4. Operations in GraphQL:
  
      - Queries: Retrieve data.
      - Mutations: Modify data (create, update, delete).
      - Subscriptions: Receive real-time updates.
## GraphQL and Security : 
 >  With the advent of new technologies, including GraphQL, new security vulnerabilities also emerge. A key point to note is that GraphQL does not include authentication mechanisms by default. It's the responsibility of developers to       implement such security measures. Without proper authentication, GraphQL endpoints may expose sensitive information to unauthenticated users, posing a significant security risk.

## GraphQL vs. REST API

| Feature                | GraphQL                                 | REST API                               |
|------------------------|-----------------------------------------|----------------------------------------|
| **Data Fetching**       | Clients request exactly what they need.  | Fixed endpoints return predefined data.|
| **Over-Fetching**       | Minimizes over-fetching by selecting fields. | Often returns more data than needed.  |
| **Under-Fetching**      | Avoids under-fetching with precise queries. | May require multiple requests.         |
| **Endpoints**           | Uses a **single endpoint** (e.g., `/graphql`). | Multiple **endpoints** for resources. |
| **Data Structure**      | Defined by a **schema** (strongly typed). | Defined by multiple endpoints.         |
| **Operations**          | Supports **queries**, **mutations**, and **subscriptions**. | Uses **HTTP methods** (GET, POST, PUT, DELETE). |
| **Performance**         | Efficient for **complex, nested** data.  | Simple for **static** resources.       |
| **Error Handling**      | Returns errors in the **response body**.  | Uses **HTTP status codes** (e.g., 404, 500). |
| **Versioning**          | **No versioning**—schema evolves over time. | Requires explicit **versioning** (e.g., `/v1`). |
| **Caching**             | Requires **custom caching** strategies.   | Supports standard **HTTP caching**.    |
| **Real-Time Updates**   | Supports **subscriptions** for live data. | Requires external methods (e.g., WebSockets). |
| **Security**            | Requires **field-level** access control.  | Simpler **endpoint-level** access control. |

## Directory Brute Force Attacks and GraphQL: 
To identify exposed GraphQL instances, the inclusion of specific paths in directory brute force attacks is recommended. These paths are:

```
/graphql
/graphiql
/graphql.php
/graphql/console
/api
/api/graphql
/graphql/api
/graphql/graphql
```
## Universal queries :
> To check if a URL is a GraphQL service, a universal query, query{__typename}, can be sent. If the response includes {"data": {"__typename": "Query"}}, it confirms the URL hosts a GraphQL endpoint. This method relies on GraphQL's __typename field, which reveals the type of the queried object.

```javascript

query{__typename}
```
##  What is Introspection in GraphQL?

**Introspection** in GraphQL is a feature that allows clients to query the **schema** itself. This means you can retrieve information about available types, queries, mutations, and fields.

###  How Introspection Works:
You can send a special GraphQL query to the server to explore its schema.

Example: Retrieve all types and their fields:

```graphql
{
  __schema {
    types {
      name
      fields {
        name
      }
    }
  }
}
```
## Testing Graphql :
### Tools :
  1. Altair Graphql (looks like postman)
  2. inQl
  3. graphql map
  4. graph ql path enum
  5. Graphql developer tool extention
  6. graphql voyager
## Reports :
  1. https://hackerone.com/reports/980511
  2. https://hackerone.com/reports/419883
  3. https://hackerone.com/reports/724944
  4. https://hackerone.com/reports/357485
  5. https://hackerone.com/reports/435066
  6. https://hackerone.com/reports/707433
  7. https://hackerone.com/reports/960244
  8. https://hackerone.com/reports/858671

## Resources :
المصادر / Sources:
1. Read:
  - [https://book.hacktricks.xyz/network-s...](https://book.hacktricks.wiki/en/network-services-pentesting/pentesting-web/graphql.html)
  - [https://portswigger.net/web-security/...](https://portswigger.net/web-security/graphql)
2. Watch:
  - (https://www.youtube.com/watch?v=eIQh02xuVw4)
  - https://www.youtube.com/watch?v=jyjGneKJynk
  - (https://www.youtube.com/watch?v=OQCgmftU-Og)
  - (https://www.youtube.com/watch?v=tJtNTqviOGg)


    


  
