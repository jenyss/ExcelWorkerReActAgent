# Excel Worker ReAct (Reasoning and Acting) AI Agent using LangChain

This Agent enables analysis of Excel files using free-form queries as user input. 

> **Note:** This is an older LangChain-based implementation. I recommend re-creating it using LangGraph or checking out this [Google ADK implementation](https://github.com/jenyss/google-adk-voice-to-visualization-agent).

If you have any questions or would like to collaborate, feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/jenya-stoeva-60477249/). You're more than welcome!

**Core Architecture**
* Built with the ReAct (Reasoning and Acting) agent pattern using LangChain
* Uses GPT-4o as the underlying LLM
* Integrates DuckDB and Pandas for structured data processing

**Main Tools**
* **preview_excel_structure**: Analyzes the file structure and data types
* **complex_duckdb_query**: Handles complex SQL operations (grouping, aggregations)
* **simple_dataframe_query**: Executes row-level operations using Pandas

**Key Features**
* Robust error handling and state management
* Intelligent handling of NULL/empty values
* Automatic data preprocessing
* Supports complex SQL queries with WITH clauses
* Built-in data visualization capabilities
* Very well decorated print line allowing to follow the execution logic

**ReAct pattern guides the workflow**
* **Input**: Excel file and a free-form user query.
* **Intermediate Step**: The agent determines which tools to call and the best approach to answering the original user question.
* **Output**: Execution result from the LLM generated query, answering the user query.

## Intallation

<b>Prerequisites</b>

* Access to <b>JupyterLab, Google Colab</b>, or another interactive computing environment to run this Jupyter Notebook.
* Access to LLM API.

### Step 1: Clone the Repository

Clone this repository to your local machine:
```
git clone <REPOSITORY_URL>
cd <PROJECT_FOLDER>
```

### Step 2: Open Jupyter Notebook in JupyterLab

Ensure that ```<PROJECT_FOLDER>``` is accessible in JupyterLab by setting it as your working directory in JupyterLab.
 * In JupyterLab, use the "Open from Path" option to load ```ExcelWorkerReActAgent.ipynb```.
 * Similarly, load ```.env``` and populate the variable keys with appropriate values.
 * The first cell in the Notebook installs the required libraries: **%pip install langchain langgraph pandas python-dotenv duckdb**

### Step 3: Run the Jupyter Notebook

To execute the notebook, select each cell and press ```Shift + Enter```.
