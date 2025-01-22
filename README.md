# ExcelWorkerReActAgent

This is a specialized data analysis agent designed to process and analyze Excel files intelligently.

**Core Architecture**
* Built with the ReAct (Reasoning and Acting) agent pattern using LangChain
* Uses GPT-4o as the underlying LLM
* Integrates DuckDB and Pandas for structured data processing

**Main Tools**
* preview_excel_structure: Analyzes the file structure and data types
* complex_duckdb_query: Handles complex SQL operations (grouping, aggregations)
* simple_dataframe_query: Executes row-level operations using Pandas

**Key Features**
* Robust error handling and state management
* Intelligent handling of NULL/empty values
* Automatic data preprocessing
* Supports complex SQL queries with WITH clauses
* Built-in data visualization capabilities
