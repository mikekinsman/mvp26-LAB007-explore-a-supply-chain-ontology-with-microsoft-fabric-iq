[← Previous: Run GQL queries](05-run-gql-queries.md) | [Next: Wrap-up →](07-wrap-up.md)

# Exercise 6: Try the Data Agent

In this step, you see how a Fabric Data Agent uses the ontology to answer natural-language questions about your data.

> [!NOTE]
> Data Agent is in preview. Expect the following behavior:
>
> - The first query often takes longer or might time out. Run it again if this happens.
> - Results might be inconsistent between runs.
> - Complex questions might not return useful answers.
>
> This step is illustrative. It demonstrates the *direction* of the technology, not production-ready behavior.

## Create a Data Agent

1. Return to your workspace.
1. Select **+ New item** and choose **Data Agent**.
1. Name the agent (for example, *RetailSupplyChainAgent*).
1. In the agent configuration, add the ontology as a data source.

## Ask questions

Try the following questions one at a time. After entering each question, wait for the response before asking the next one.

**Question 1:**

> What is the loyalty tier and lifetime value for Customer CUST000297?

Review the response. The agent should return the customer's loyalty tier and lifetime value by querying through the ontology.

**Question 2:**

> Is Region southwest marked as cold-chain required, and what is its timezone?

This question tests the agent's ability to find specific attributes on a Region entity.

**Question 3:**

> For Customer CUST000297, show the customer's region name and the latest customer engagement score.

This question requires the agent to traverse a relationship from Customer to Region, demonstrating cross-entity reasoning.

> [!NOTE]
> If a query times out or returns an error, try running it again. First queries in a new Data Agent session often fail. This is a known limitation of the preview.

---

[← Previous: Run GQL queries](05-run-gql-queries.md) | [Next: Wrap-up →](07-wrap-up.md)
