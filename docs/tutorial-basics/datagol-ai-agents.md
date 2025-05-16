---
sidebar_position: 2
---

# DataGOL AI Agents

## About DataGOL AI agents

The DataGOL AI Agents empower business users and engineers to efficiently analyze and visualize data through a suite of specialized AI agents. These agents act as intelligent assistants, guiding users through the data exploration process and accelerating insights.

DataGOL provides the following AI agents, each designed for specific tasks:

- **Data Conversion (DC) Agent**: The default agent, excels at answering questions about your data using SQL queries. Ideal for filtering, sorting, grouping, and performing calculations on structured data.  
  <img src="/img/Screenshot-2025-05-12-at-3.09.07-PM.png" alt="Data Conversion Agent" />

- **BI (Chart) Agent**: Specializes in generating insightful visualizations from your data, including bar charts, pie charts, line graphs, and more.  
  <img src="/img/Screenshot-2025-05-12-at-3.08.40-PM.png" alt="BI Agent" />

- **Python Agent**: Enables advanced analysis by generating and executing Python scripts. Maintains conversation history for contextual awareness.

- **RAG Agent**: Handles unstructured data like PDFs, PPTX, DOCX, images, and videos, and extracts relevant information.  
  <img src="/img/Screenshot-2025-05-12-at-3.07.23-PM-20250512-190729.png" alt="RAG Agent" />

- **SQL Agent**: Generates, optimizes, and debugs SQL queries using natural language prompts.

- **Data Cleaning (DC) Agent**: Designed to clean and organize data within a workbook.

---

## Key user considerations

- **Agents on structured data**: Tailored to the workbook currently selected.
- **Agent selection**: Choose the agent best suited for your desired output.
- **Data relevance**: Context is based on the loaded dataset.
- **Feedback**: Crucial for improving the agents.

---

## Enabling the agents

Enable/Disable one or more agents from the admin console.

---

## Data Conversion Agent (DCA) - Default

### Key features

- Natural language querying
- SQL query generation
- Tabular Output
- Transparency of query logic
- Filtering, sorting, aggregation
- Outlier detection
- Automatic routing to chart agent

### Use cases

- Finding data points
- Trend analysis
- Report generation
- Outlier detection

### Limitations

- Structured data only
- SQL dependent
- Imperfect keyword routing

### User interaction

- Text-based chat interface
- Results in table/text format
- SQL code visibility
- Chart suggestions
- Downloadable results
- Subview creation
- Editable queries (human-in-the-loop)

---

## Business Intelligence (BI) agent - Chart agent

### Key features

- Bar, pie, line, stacked bar charts
- Multiple Y-axis
- Filter display
- Data distribution and time-series support
- Dashboard visual attachment

### Use Cases

- Visual trends and patterns
- Dashboards
- Easy-to-understand data presentation

### Limitations

- Limited interactivity
- Does not support all chart types

### User Interaction

- Enter chart-specific queries
- Displayed within chat, pinnable to dashboards

---

## Python agent - Advanced data analysis

### Purpose

- Sophisticated data analysis using Python
- Advanced statistics and data science tasks

### Key Features

- Python library use (Pandas, Sklearn)
- Forecasting and prediction
- Model application
- Complements DCA and BI

### Use Cases

- In-depth analysis
- ML code generation
- PCA/dimensionality reduction
- Anomaly detection

---

## Retrieval Augmented Generation (RAG) Agent

### Key features

- Knowledge base integration
- Supported formats: PDF, DOC, TXT, PPT
- Accurate + efficient retrieval
- JSON/table formatting
- Chunk references
- Custom agents: Invoice Analyzer, Clinical Report Analyzer

### Specific capabilities

- Simple Q&A
- Detail extraction
- Comparison
- Formatting

### Workflow

1. Upload documents.
2. Select RAG agent.
3. Ask questions.
4. System processes (chunk/index).
5. Receive answer with references.

### Limitations & Future Enhancements

- Preview: Only for PDFs (others coming)
- Chunk highlighting planned
- Knowledge source linking
- MP3/MP4 support
- API/SDK
- Custom agent builder
- Orchestrator copilot

---

## FAQ

**Can I upload documents in languages other than English?**  
Yes.

**Does the DC agent work with documents?**  
No, use RAG agent.

**Is there a limit to uploads?**  
No hard limit; processing time increases with size.

**Can I switch agents?**  
Yes.

**Can I delete documents?**  
Yes, via "View All".

---

## SQL Agent

### Key Features

- Natural language to SQL
- Query optimization
- Debugging tools
- Integrated in DataGOL
- User-friendly UI

---

## Data Cleaning (DC) Agent

### Key Features

- Deduplication
- Normalization
- Data imputation
- Filtering
- Conversational interaction
- Data overview
- Downloadable output
- Reset option

### How to Use

1. Select DC Agent.
2. Upload Excel/CSV.
3. Use commands like:
   - `"help me dedup"`
   - `"fill 999 999 999"`
   - `"show me records with agent name Henry Madlin"`
   - `"help me normalize"`
4. Review, download, or reset cleaned data.

### Example Usage

- **Deduplication**: `"help me dedup using agent name, policy number"`
- **Data Imputation**: `"fill missing phone numbers with 999-999-9999"`
- **Filtering**: `"show me records where agent name is John Doe"`
- **Normalization**: `"help me normalize the data"`
