# Level 0: GraphQL Fundamentals (Task 0 and Task 1)

This documentation covers the completion of **Task 0 (Single Character Retrieval)** and **Task 1 (Paginated List Retrieval)**, which form the foundational stage of the project designed to build proficiency in GraphQL.

## 1. Project Overview: GraphQL Fundamentals

The primary goal of Level 0 is to learn how to **construct precise GraphQL queries to request specific data**, thereby maximizing efficiency and performance.

### Key GraphQL Concepts Demonstrated:

*   **GraphQL Defined:** GraphQL is a **query language** for APIs and a runtime for executing queries. It was developed by **Facebook**.
*   **Efficiency:** A key advantage of GraphQL is its ability to eliminate the problem of **over-fetching** (receiving more data than necessary) and **under-fetching** data. By allowing clients to specify exactly what data they need, it reduces unnecessary data transfer, enhancing network efficiency and application performance.
*   **Single Endpoint:** Unlike traditional REST APIs where each resource typically has its own endpoint, GraphQL retrieves all data from a **single endpoint**.
*   **Arguments:** Arguments are used in GraphQL to be specific in data requests, allowing for filtering and pagination (e.g., using `id` or `page`).

## 2. Task 0: Write a Query to Get a Specific Character by ID

**Objective:** To write a GraphQL query to retrieve a specific character’s information using their unique identifier. This task demonstrates querying for a single item.

### Implementation Details:

1.  **Field and Arguments:** The query uses the `character(id: ID!)` field. The argument `id: ID!` signifies that the ID is a **required ID variable** (non-nullable).
2.  **Scope:** Queries were generated for character IDs **1, 2, 3, and 4**.
3.  **Data Fields:** To ensure efficiency and avoid over-fetching, only the necessary fields were requested: `id`, `name`, `status`, `species`, `type`, and `gender`.

### Example Query Structure (Character ID 1):

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

## 3. Task 1: Write a Query to Get a List of All Characters

**Objective:** To create a GraphQL query to retrieve a paginated list of all characters. This demonstrates handling large datasets via **pagination**.

### Implementation Details:

1.  **Field and Arguments:** The query uses the `characters(page: Int)` field. The `page` argument is crucial for navigating through the results. This task required differentiating between querying for a single item (Task 0) and a paginated list of items.
2.  **Scope:** Queries were generated for pages **1, 2, 3, and 4**.
3.  **Data Fields:** The query selects the list results and the necessary subfields, specifically requesting: `id`, `name`, `status`, and `image`.

### Example Query Structure (Character Page 1):

```graphql
query {
  characters(page: 1) {
    info {
      pages
      next
      prev
      count
    }
    results {
      id
      name
      status
      image
    }
  }
}
```

## 4. Mandatory Files (Combined List)

All files for Task 0 and Task 1 are located in the `alx-graphql-0x00/character` directory. The `.json` files represent the exact API response for the corresponding query, confirming successful execution and adherence to the requested data structure.

| File Name | Description | Source |
| :--- | :--- | :--- |
| `README.md` | This combined documentation file. | |
| `character-id-1.graphql` | GraphQL query for Character ID 1. | |
| `character-id-1-output.json` | JSON output of the API response for Character ID 1. | |
| `character-id-2.graphql` | GraphQL query for Character ID 2. | |
| `character-id-2-output.json` | JSON output of the API response for Character ID 2. | |
| `character-id-3.graphql` | GraphQL query for Character ID 3. | |
| `character-id-3-output.json` | JSON output of the API response for Character ID 3. | |
| `character-id-4.graphql` | GraphQL query for Character ID 4. | |
| `character-id-4-output.json` | JSON output of the API response for Character ID 4. | |
| `characters-page-1.graphql` | GraphQL query for Character List Page 1. | |
| `characters-page-1-output.json` | JSON output of the API response for Character Page 1. | |
| `characters-page-2.graphql` | GraphQL query for Character List Page 2. | |
| `characters-page-2-output.json` | JSON output of the API response for Character Page 2. | |
| `characters-page-3.graphql` | GraphQL query for Character List Page 3. | |
| `characters-page-3-output.json` | JSON output of the API response for Character Page 3. | |
| `characters-page-4.graphql` | GraphQL query for Character List Page 4. | |
| `characters-page-4-output.json` | JSON output of the API response for Character Page 4. | |
