# LangChain ReAct Agent Project

This project demonstrates the implementation of **ReAct (Reasoning and Acting)** agents using LangChain, showcasing both general-purpose agents with multiple tools and specialized SQL database agents.

## Overview

ReAct is a framework that combines reasoning and acting in language models. This project contains two main implementations:

1. **General ReAct Agent** - An agent equipped with web search, Wikipedia, and custom enterprise tools
2. **SQL Database Agent** - A specialized agent that can query and analyze a SQLite sales database

## Project Structure

```
ReAct/
├── 1.ReAct_Agnet_intro.ipynb    # Introduction to ReAct agents with multiple tools
├── 2.ReAct_DB_Agent.ipynb       # SQL database agent implementation
├── init_db.py                    # Database initialization script
├── demo.py                       # Simple database query demonstration
├── SalesDB/
│   └── sales.db                  # SQLite database with sales data
├── .env                          # Environment variables (API keys)
└── .gitignore                    # Git ignore configuration
```

## Features

### 1. General ReAct Agent

- **DuckDuckGo Search Tool**: Search the web for recent news and information
- **Wikipedia Tool**: Query Wikipedia for encyclopedic information
- **Custom Enterprise Tool**: Example custom tool for sending emails
- **Streaming Support**: Real-time streaming of agent responses

### 2. SQL Database Agent

- Query sales database using natural language
- Automatic SQL query generation
- Built-in tools provided by SQLDatabaseToolkit
- Support for complex analytical queries

## Prerequisites

- Python 3.8+
- Required packages:
  - `langchain`
  - `langchain-community`
  - `langchain-groq`
  - `ddgs` (DuckDuckGo Search)
  - `wikipedia`
  - `python-dotenv`
  - `sqlite3` (included with Python)

## Installation

1. Install the required packages:

```bash
pip install langchain langchain-community langchain-groq ddgs wikipedia python-dotenv
```

2. Create a `.env` file in the ReAct directory with your API key:

```
GROQ_API_KEY=your_groq_api_key_here
```

## Setup

### Initialize the Database

Run the initialization script to create and populate the sales database:

```bash
python init_db.py
```

This creates a SQLite database with an `orders` table containing:

- Customer information
- Product names
- Quantities
- Prices and totals

### Sample Database Schema

```sql
CREATE TABLE orders (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    customer_name TEXT NOT NULL,
    product_name TEXT NOT NULL,
    quantity INTEGER NOT NULL,
    price REAL NOT NULL,
    total REAL NOT NULL
)
```

### Sample Data

- John Doe - Laptop (1 unit, $1000.00)
- Jane Smith - Smartphone (2 units, $1000.00)
- Alice Johnson - Headphones (3 units, $300.00)

## Usage

### Running the Demo Script

To verify the database setup, run:

```bash
python demo.py
```

This will display all orders in the database.

### Using the Notebooks

Start Jupyter Notebook and explore:

1. **1.ReAct_Agnet_intro.ipynb**: Learn how to create a ReAct agent with multiple tools
   - Set up different tools (search, Wikipedia, custom)
   - Create and configure the agent
   - Stream agent responses in real-time
   - Manually bind LLM with tools

2. **2.ReAct_DB_Agent.ipynb**: Work with database agents
   - Connect to SQLite database
   - Create SQL database toolkit
   - Query database using natural language
   - Example: "How much sales we made for SmartPhone"

## Example Queries

### General Agent

- "What are latest news of Sri Lanka?"
- "Who is [person name]?"
- "Tell me about [topic] from Wikipedia"

### Database Agent

- "How much sales we made for SmartPhone?"
- "Who bought the most expensive item?"
- "What is the total revenue from all orders?"
- "List all customers who bought headphones"

## Key Concepts

### ReAct Pattern

ReAct agents follow a "Thought → Action → Observation" loop:

1. **Thought**: The agent reasons about what to do next
2. **Action**: Executes a tool or provides an answer
3. **Observation**: Processes the result and continues or concludes

### Tool Binding

The project demonstrates two approaches:

- Using `create_agent()` for automatic tool integration
- Manually binding tools with `llm.bind_tools()` for custom behavior

### Streaming Mode

Both agents support streaming responses, allowing real-time observation of the agent's reasoning process.

## Model Configuration

The project uses **Groq's LLama 3.3 70B Versatile** model with:

- Temperature: 0.1-0.7 (depending on use case)
- Max tokens: 1000
- Timeout: 30 seconds

You can modify these parameters in the notebooks based on your requirements.

## Troubleshooting

### Common Issues

1. **SQL Syntax Error**: Ensure `init_db.py` has no trailing commas in the CREATE TABLE statement
2. **Missing API Key**: Verify `.env` file contains valid `GROQ_API_KEY`
3. **Tool Import Errors**: Ensure all required packages are installed
4. **Database Not Found**: Run `init_db.py` before using the database agent

## Contributing

Feel free to extend this project by:

- Adding more custom tools
- Expanding the database schema
- Implementing additional agent types
- Experimenting with different LLMs

## License

This project is for educational purposes as part of the LangChain learning series.

## Resources

- [LangChain Documentation](https://python.langchain.com/)
- [ReAct Paper](https://arxiv.org/abs/2210.03629)
- [Groq API Documentation](https://groq.com/)

---

**Note**: This is part of a larger LangChain tutorial series (v1). Check the parent directory for more examples and learning materials.
