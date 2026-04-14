# Exercise 1: Deploy the environment

A single Fabric notebook deploys all the artifacts you need for this lab, including:

- An Eventhouse named **EHRetail** with pre-populated tables
- A Lakehouse named **LHRetail** with supporting data
- An ontology with entity types, relationship types, and data bindings

## Upload and run the setup notebook

1. Open the `Initial_Lab_Deployment 1.ipynb` notebook file from the root of this repository. If you haven't already, clone the repository or open it in a GitHub Codespace.
1. Open your Fabric workspace.
1. Select **+ New item** > **Import notebook**.
1. Select **Upload** and browse to the notebook file, then select **Open**.
1. Wait for the upload to complete. The notebook appears in your workspace item list.
1. Open the uploaded notebook.
1. Select **Run all** to execute the notebook.

   The notebook performs the following actions automatically:
   - Creates the Eventhouse and Lakehouse artifacts
   - Generates sample retail data across all tables
   - Creates the ontology with entity types and relationships
   - Binds entity types to data sources
   - Triggers a graph refresh

   > [!IMPORTANT]
   > The graph refresh runs in the background and takes approximately 10–15 minutes to complete. You cannot accelerate this process. Continue to the next steps while it runs.

1. Confirm that the notebook cells complete without errors. You should see success messages for each artifact creation step.

---

**Next:** [Exercise 2: Understand IQ and ontology concepts](02-understand-iq-concepts.md)
