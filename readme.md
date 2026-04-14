# [MVP Summit 2026](https://mvp.microsoft.com)

## 🔥 LAB007: Build a Supply Chain Ontology with Microsoft Fabric IQ

### Lab Description

Gain practical, end-to-end experience in building and querying a supply chain ontology with Microsoft Fabric IQ. Participants will leverage the platform's semantic layer to transform raw data into shared business understanding, enabling both teams and AI agents to reason, decide, and act in the language of the business. The lab demonstrates how Fabric IQ's capabilities accelerate decision-making and business insights.

### 🚀 Getting Started

To get started with this lab at your own pace:

1. Clone this repository to your local machine or open it in a GitHub Codespace.
1. Ensure you have access to a [Microsoft Fabric](https://learn.microsoft.com/fabric/get-started/microsoft-fabric-overview) workspace with capacity enabled.
1. Open the `Initial_Lab_Deployment 1.ipynb` notebook file from the root of this repository.
1. In your Fabric workspace, select **+ New item** > **Import notebook**, then upload the notebook file.
1. Open the uploaded notebook and select **Run all** to deploy the lab environment (Eventhouse, Lakehouse, ontology, and sample data).
1. Wait for the graph refresh to complete (approximately 10–15 minutes).
1. Follow the step-by-step lab exercises in the [docs/](docs/index.md) folder, starting with the [lab overview](docs/index.md).

### 🧠 Learning Outcomes

By the end of this lab, you will be able to:

- Understand how Microsoft Fabric IQ uses ontologies to unify data across multiple storage engines (Eventhouse and Lakehouse) under shared business concepts
- Explore a graph-based data model visually, navigating entity types, relationships, and data bindings in the Fabric IQ interface
- Write and execute GQL (Graph Query Language) queries to traverse ontology relationships and answer complex business questions across data sources
- Use a Fabric Data Agent to ask natural-language questions against an ontology and observe how the agent reasons over graph data

### 💬 Keep Learning with Copilot

Try these prompts with GitHub Copilot to explore the topics from this lab. Open Copilot Chat in Visual Studio Code (`Ctrl+Alt+I` on Windows/Linux, `Cmd+Shift+I` on Mac), paste a prompt, and see what you learn. Try connecting the [Microsoft Learn MCP Server](#-microsoft-learn-mcp-server) for the latest official documentation.

1. Understand ontology basics:

```
Using the Microsoft Learn MCP Server, explain what an ontology is in Microsoft Fabric IQ and how it differs from a traditional relational data model. What problems does it solve for enterprise data?
```

2. Go deeper with GQL:

```
Using the Microsoft Learn MCP Server, find the GQL language guide for Microsoft Fabric. Explain the key differences between GQL MATCH patterns and SQL JOINs, and show an example of traversing three entity types in a single query.
```

3. Build on the lab scenario:

```
I just completed a lab where I built a retail supply chain ontology in Microsoft Fabric IQ with entities like Order, Product, Customer, and Region. Help me design an extension to this ontology that adds Supplier and PurchaseOrder entity types, including the relationship types that would connect them to the existing entities.
```

### 💻 Technologies Used

1. [Microsoft Fabric](https://learn.microsoft.com/fabric/get-started/microsoft-fabric-overview) — Unified analytics platform for data engineering, data science, real-time analytics, and business intelligence
1. [Fabric IQ (preview)](https://learn.microsoft.com/fabric/iq/overview) — Semantic layer that enables ontology-based data modeling and reasoning
1. [Ontology in Fabric IQ](https://learn.microsoft.com/fabric/iq/ontology/overview) — Entity types, relationship types, and data bindings that map business concepts to underlying data
1. [Eventhouse](https://learn.microsoft.com/fabric/real-time-intelligence/eventhouse) — Real-time analytics engine for operational and streaming data
1. [Lakehouse](https://learn.microsoft.com/fabric/data-engineering/lakehouse-overview) — Batch and historical data storage combining data lake and data warehouse capabilities
1. [Graph in Microsoft Fabric](https://learn.microsoft.com/fabric/graph/overview) — Graph visualization and exploration of ontology entities and relationships
1. [GQL (Graph Query Language)](https://learn.microsoft.com/fabric/graph/gql-language-guide) — ISO-standardized query language for traversing graph data
1. [Fabric Data Agent](https://learn.microsoft.com/fabric/data-science/concept-data-agent) — AI-powered conversational interface for querying data through natural language

### 📚 Resources and Next Steps

| Resource | Description |
|:---------|:------------|
| [What is Fabric IQ (preview)?](https://learn.microsoft.com/fabric/iq/overview) | Overview of Fabric IQ capabilities and concepts |
| [What is ontology (preview)?](https://learn.microsoft.com/fabric/iq/ontology/overview) | Introduction to ontology modeling in Fabric IQ |
| [Ontology (preview) tutorial](https://learn.microsoft.com/fabric/iq/ontology/tutorial-0-introduction) | Step-by-step tutorial for building your own ontology |
| [Graph in Microsoft Fabric](https://learn.microsoft.com/fabric/graph/overview) | Overview of graph capabilities in Fabric |
| [GQL language guide](https://learn.microsoft.com/fabric/graph/gql-language-guide) | Full reference for the GQL query language in Fabric |
| [GQL expressions, predicates, and functions](https://learn.microsoft.com/fabric/graph/gql-expressions) | Detailed reference for GQL syntax elements |
| [Fabric Data Agent](https://learn.microsoft.com/fabric/data-science/concept-data-agent) | Documentation for the AI-powered Data Agent |

### 🌟 Microsoft Learn MCP Server

[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Microsoft_Docs_MCP-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect/mcp/install?name=microsoft.docs.mcp&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Flearn.microsoft.com%2Fapi%2Fmcp%22%7D)

The Microsoft Learn MCP Server is a remote MCP Server that enables clients like GitHub Copilot and other AI agents to bring trusted and up-to-date information directly from Microsoft's official documentation. Get started by using the one-click button above for Visual Studio Code or access the [mcp.json](.vscode/mcp.json) file included in this repo.

For more information, setup instructions for other dev clients, and to post comments and questions, visit our Learn MCP Server GitHub repo at [https://github.com/MicrosoftDocs/MCP](https://github.com/MicrosoftDocs/MCP). Find other MCP Servers to connect your agent to at [https://mcp.azure.com](https://mcp.azure.com).

*Note: When you use the Learn MCP Server, you agree with [Microsoft Learn](https://learn.microsoft.com/en-us/legal/termsofuse) and [Microsoft API Terms](https://learn.microsoft.com/en-us/legal/microsoft-apis/terms-of-use) of Use.*

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit [Contributor License Agreements](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
