# Task 0: Write a Query to Get a Specific Character by ID

This task is part of the **Level 0: GraphQL Fundamentals** learning journey of the project, focusing on constructing precise GraphQL queries to request specific data.

## 1. Overview and Key Concepts

The primary goal of this task is to demonstrate the ability to construct an efficient GraphQL query that fetches details for a single character using a specific identifier (ID).

GraphQL is a **query language** for APIs that allows clients to request **exactly the data they need**. This capability is a key strength, as it allows developers to define precisely what data they require, which eliminates the common issue of **over-fetching** unnecessary data often associated with traditional REST APIs. This optimized approach enhances overall application performance and efficiency.

## 2. Implementation Details

### Query Objective

The objective was to write a GraphQL query to retrieve a specific character’s information using their ID.

### Required Fields and Arguments

1.  **Field Selection:** The query utilizes the specific field `character(id: ID!)` to retrieve a single character item.
2.  **Required Argument:** The `id` is passed as an **argument** to be specific in the data request. The `!` (exclamation mark) in the definition `ID!` denotes that this argument is **non-nullable** and **required**.
3.  **Data Requested:** By defining the specific fields within the query, we avoid transmitting unnecessary data. The required fields included in the query are: `id`, `name`, `status`, `species`, `type`, and `gender`.
4.  **Target IDs:** Queries were created and executed for character IDs **1, 2, 3, and 4**.

### Example Query Structure (Character ID 1)

```graphql
query {
  character(id: 1) {
    id
    name
    status
    species
    type
    gender
  }
}
```

## 3. Mandatory Files

All files for Task 0 are located in the `alx-graphql-0x00/character` directory. The execution of the GraphQL queries resulted in JSON files that capture the response received from the API, confirming the specified data structure was returned.

| File Name | Description |
| :--- | :--- |
| `README.md` | This documentation file. |
| `character-id-1.graphql` | GraphQL query for Character ID 1. |
| `character-id-1-output.json` | JSON output demonstrating the API response for Character ID 1. |
| `character-id-2.graphql` | GraphQL query for Character ID 2. |
| `character-id-2-output.json` | JSON output demonstrating the API response for Character ID 2. |
| `character-id-3.graphql` | GraphQL query for Character ID 3. |
| `character-id-3-output.json` | JSON output demonstrating the API response for Character ID 3. |
| `character-id-4.graphql` | GraphQL query for Character ID 4. |
| `character-id-4-output.json` | JSON output demonstrating the API response for Character ID 4. |
