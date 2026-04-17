[Next: Deploy the environment →](01-deploy-the-environment.md)

# IQ hands-on lab: Retail supply chain

In this 60-minute hands-on lab, you explore the core capabilities of [Fabric IQ (preview)](https://learn.microsoft.com/fabric/iq/overview) using a retail supply chain scenario. A single setup notebook deploys all required artifacts automatically, so you can focus on exploring ontology concepts, graph visualization, GQL queries, and Data Agent interactions.

## Scenario overview

You work for a fictional retail company that manages orders, products, customers, warehouses, and shipments across multiple regions. The company tracks inventory, demand signals, forecasts, and promotions. Your goal is to explore how Fabric IQ unifies this data using an ontology, visualizes it as a graph, and makes it queryable through GQL and conversational Data Agent.

### Why retail supply chain?

Retail supply chain is an ideal scenario for demonstrating ontology capabilities because it reflects the complexity that real enterprises face:

- **Data lives in multiple systems.** Orders might stream into an Eventhouse for real-time analytics, while product catalogs and customer profiles sit in a Lakehouse for batch processing. Traditional approaches require analysts to know which system holds which data and how to join across them.
- **Relationships are central to insight.** A single question like "Which promotions drove returns in the southwest region?" requires traversing from returns to products to promotions to regions. Flat tables make this painful; a graph makes it natural.
- **Business language differs from technical schemas.** Column names like `cust_lt_val` or `prod_cat_id` don't match how business users think. An ontology maps technical columns to concepts like *Customer lifetime value* and *Product category*, so everyone speaks the same language.
- **Multiple personas need access.** Data engineers care about schema and lineage. Analysts want to explore relationships visually. Business users want to ask questions in plain English. Ontology, graph, and Data Agent serve all three from the same foundation.

This lab walks you through each layer—from raw tables to semantic model to conversational AI—using a realistic set of retail entities and relationships.

### Entities and relationships

The ontology for this lab includes the following entity types:

| Entity type | Description |
|---|---|
| *Order* | A customer purchase transaction |
| *OrderLine* | Individual line items within an order |
| *Customer* | The buyer associated with an order |
| *Product* | Items available for sale |
| *ProductCategory* | Groupings of related products |
| *Store* | Retail locations where orders originate |
| *Region* | Geographic areas containing stores and warehouses |
| *Warehouse* | Fulfillment centers that ship orders |
| *Carrier* | Logistics providers handling shipments |
| *Shipment* | Delivery records linking orders to carriers |
| *Inventory* | Stock levels at warehouses |
| *Forecast* | Predicted demand for products |
| *DemandSignal* | Real-time indicators of customer demand |
| *Promotion* | Marketing campaigns affecting product sales |
| *Return* | Returned items linked back to orders |

Key relationships include *Order* &rarr; *Customer*, *Order* &rarr; *Region*, *OrderLine* &rarr; *Product*, *Product* &rarr; *ProductCategory*, *Shipment* &rarr; *Carrier*, and *Shipment* &rarr; *Warehouse*.

## Lab exercises

| Time | Activity | Exercise |
|---|---|---|
| 0–5 min | Run setup notebook | [Exercise 1: Deploy the environment](01-deploy-the-environment.md) |
| 5–20 min | Introduction to IQ and ontology concepts | [Exercise 2: Understand IQ and ontology concepts](02-understand-iq-concepts.md) |
| 20–35 min | Explore artifacts before graph is ready | [Exercise 3: Explore deployed artifacts](03-explore-deployed-artifacts.md) |
| 35–45 min | Graph UI exploration | [Exercise 4: Explore the graph](04-explore-the-graph.md) |
| 45–55 min | Run GQL queries | [Exercise 5: Run GQL queries](05-run-gql-queries.md) |
| 55–58 min | Data Agent demo | [Exercise 6: Try the Data Agent](06-try-the-data-agent.md) |
| 58–60 min | Wrap-up and roadmap | [Exercise 7: Wrap-up](07-wrap-up.md) |

---

[Next: Deploy the environment →](01-deploy-the-environment.md)
