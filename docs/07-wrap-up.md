[← Previous: Try the Data Agent](06-try-the-data-agent.md) | [Back to Overview](index.md)

# Exercise 7: Wrap-up

You've now explored an IQ workflow—from ontology authoring and cross-source data bindings to graph traversal, GQL queries, and conversational Data Agent. Here's a snapshot of the current state of IQ.

## What works today

- Ontology creation with entity types, properties, and relationship types
- Data bindings to Eventhouse and Lakehouse
- Graph visualization and exploration
- GQL querying
- Data Agent with ontology as a source

## Known limitations

- Graph refresh times are long and non-deterministic
- Data Agent queries can time out, especially on first run
- Data Agent results might be inconsistent between runs
- Complex natural-language queries might not return useful results

## What's coming next

- Improvements to graph refresh performance
- Enhanced Data Agent reliability and query coverage
- Additional GQL capabilities

## Clean up resources

If you're done exploring, you can delete the workspace or the individual items created during this lab to avoid incurring capacity usage:

1. Navigate to your workspace.
1. Select the items created during the lab (**EHRetail**, the Lakehouse, the ontology, and the Data Agent).
1. Delete the selected items.

## Related content

- [What is Fabric IQ (preview)?](https://learn.microsoft.com/fabric/iq/overview)
- [What is ontology (preview)?](https://learn.microsoft.com/fabric/iq/ontology/overview)
- [Ontology (preview) tutorial](https://learn.microsoft.com/fabric/iq/ontology/tutorial-0-introduction)
- [Graph in Microsoft Fabric](https://learn.microsoft.com/fabric/graph/overview)
- [GQL language guide](https://learn.microsoft.com/fabric/graph/gql-language-guide)
- [GQL expressions, predicates, and functions](https://learn.microsoft.com/fabric/graph/gql-expressions)
- [Fabric data agent](https://learn.microsoft.com/fabric/data-science/concept-data-agent)

---

[← Previous: Try the Data Agent](06-try-the-data-agent.md) | [Back to Overview](index.md)
