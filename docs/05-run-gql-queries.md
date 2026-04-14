# Exercise 5: Run GQL queries

In this step, you use GQL (Graph Query Language) to query the ontology graph directly. Before writing queries, take a moment to understand what GQL is and why it's the right tool for this scenario.

## What is GQL?

GQL is the ISO-standardized query language for graph databases ([ISO/IEC 39075](https://www.iso.org/standard/76120.html)). The same ISO working group that develops SQL also develops GQL, so you'll find familiar concepts if you've written SQL queries before—expressions, predicates, types, and filtering all work similarly.

The key difference is how you express relationships. Instead of writing JOIN statements that link tables together, GQL uses **visual graph patterns** that directly describe the connections you want to traverse. This makes queries more readable and closer to how you naturally think about connected data.

## Why use GQL for ontology queries?

Traditional SQL excels at finding data within a single table or joining a small number of related tables. But when you need to traverse many relationships—like finding which promotions drove returns in a specific region—SQL queries become complex chains of joins that are difficult to write and harder to maintain.

GQL solves this problem by treating relationships as first-class citizens. A query that would require five or six JOIN statements in SQL becomes a single pattern that reads almost like a sentence: "find customers who placed orders that contained products in a specific category."

In the context of Fabric IQ, GQL lets you:

- **Traverse ontology relationships naturally.** The pattern `(node:EntityType)-[edge:RelationshipType]->(node:EntityType)` mirrors exactly how you defined relationships in the ontology.
- **Query across data sources transparently.** The same GQL query can traverse from data in the Eventhouse to data in the Lakehouse without you needing to know which engine holds which entity.
- **Express complex business questions concisely.** Questions like "Which customers in the southwest region ordered products from promotions that had returns?" become single, readable queries.

## What works today

GQL support in Fabric IQ includes:

- **MATCH patterns** for traversing nodes and edges across entity types and relationship types
- **WHERE clauses** for filtering results based on property values
- **RETURN statements** for specifying which data to output
- **Pattern composition** for combining multiple relationship paths in a single query
- **Aggregations** for counting, summing, and grouping results

## Current limitations

GQL support is in preview, so expect the following:

- **Query complexity limits.** Very long traversal paths (more than six or seven hops) may time out or return incomplete results.
- **No schema modifications from GQL.** You can't create or modify entity types, relationship types, or bindings using GQL—use the ontology UI for schema changes.
- **Limited function support.** Some advanced GQL functions from the ISO standard aren't yet available.

For the full GQL language reference in Fabric, see [GQL language guide](https://learn.microsoft.com/fabric/graph/gql-language-guide).

## Run your first GQL query

1. Select **Clear query** to reset the graph query.
1. Copy and paste the following GQL query into the code editor. This query finds all customers in the southwest region who placed orders for products in the household category. It traverses from *Customer* through *Order* and *OrderLine* to *Product*, then branches to both *ProductCategory* and *Region* to apply filters.

   ```gql
   MATCH (node_Order:`Order`)-[edge1_OrderFulfilledToRegion:`OrderFulfilledToRegion`]->(node_Region:`Region`),
       (node_Order:`Order`)-[edge2_OrderPlacedByCustomer:`OrderPlacedByCustomer`]->(node_Customer:`Customer`),
       (node_OrderLine:`OrderLine`)-[edge3_OrderHasLineItem:`OrderHasLineItem`]->(node_Order:`Order`),
       (node_OrderLine:`OrderLine`)-[edge4_OrderLineReferencesProduct:`OrderLineReferencesProduct`]->(node_Product:`Product`),
       (node_Product:`Product`)-[edge5_ProductInCategory:`ProductInCategory`]->(node_ProductCategory:`ProductCategory`)
   WHERE node_Region.`RegionName` = "southwest"
       AND node_ProductCategory.`CategoryName` = "household"
   RETURN TO_JSON_STRING(node_Customer) AS `Customer`
   ```

1. Select **Run** to execute the query.
1. Review the results. The query returns customers from the southwest region whose orders included products in the household category. Notice how the GQL pattern mirrors the ontology relationships you explored earlier—each `[edge:RelationshipType]` corresponds to a relationship type you defined in the ontology.

> [!TIP]
> As you review query results, pay attention to how GQL traverses relationships. The pattern `(node:EntityType)-[edge:RelationshipType]->(node:EntityType)` mirrors the ontology structure. This is the power of a graph-based semantic model—queries follow the natural structure of your business concepts.

---

**Next:** [Exercise 6: Try the Data Agent](06-try-the-data-agent.md)
