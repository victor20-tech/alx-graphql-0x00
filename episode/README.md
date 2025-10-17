# Task 2: Write a Query to Get a Specific Episode by ID

## Repository and Location
**Repository:** `alx-graphql-0x00`
**Directory:** `episode`
**Required Files:** `README.md`, `episode-page-1.graphql` (and related output files).

## Objective
The objective of this task is to **write a precise GraphQL query** to fetch the specific details of a single episode, identified by its ID.

This exercise is part of **Level 0 (GraphQL Fundamentals)**, focusing on constructing precise queries to request specific data and using arguments to filter results.

## GraphQL Fundamentals Applied

GraphQL is a powerful alternative to traditional REST APIs. It is a query language that allows clients to fetch data from APIs. Its fundamental difference is that it allows clients to **specify exactly how to structure the data** when it is returned by the server.

1.  **Flexibility and Efficiency:** By specifying only the required fields, this approach eliminates the issue of **over-fetching** unnecessary data. This results in improved network efficiency, reduced payload sizes, and enhanced application performance.
2.  **Arguments:** Unlike requesting a list, accessing a single item requires using **arguments** (like `id` or `page`) to filter and be specific in the data request.
3.  **Single Request:** GraphQL allows all data to be retrieved from a **single endpoint**.

## Instructions

1.  Write a GraphQL query using the `episode(id: ID!)` field to retrieve the details of a specific episode.
2.  Ensure that your query only includes the following fields for the episode:
    *   `id`
    *   `name`
    *   `air_date`
    *   `episode` (which typically contains the episode code, e.g., S01E01)

## Example Query Structure

To fetch a specific episode (using ID 1 as an example), the query structure must utilize the `episode` root field along with the required `id` argument, followed by the specific fields needed:

```graphql
query {
  episode(id: 1) {
    id
    name
    air_date
    episode
  }
}
```

By requesting only these four fields, you demonstrate the core efficiency benefit of GraphQL.
```