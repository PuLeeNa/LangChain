# LangChain Learning Repository

A comprehensive collection of Jupyter notebooks and examples for learning **LangChain** - the popular framework for building applications with Large Language Models (LLMs).

## 📚 Overview

This repository contains hands-on tutorials and examples covering LangChain versions 0.3 and 1.x, progressing from basic concepts to advanced topics like agents, chains, streaming, and database integration.

## 🗂️ Repository Structure

```
LangChain/
├── v0.3/                           # LangChain v0.3 tutorials
│   ├── 1.intro.ipynb               # Introduction to LangChain
│   ├── 2.prompts.ipynb             # Prompt engineering
│   ├── 3.Chat_Memory.ipynb         # Chat memory and context
│   ├── 4_Agents_intro.ipynb        # Introduction to agents
│   ├── 5_Agent_Deep_Dive.ipynb     # Advanced agent concepts
│   ├── 6_LCEL.ipynb                # LangChain Expression Language
│   ├── 6_LCEL_part_2.ipynb         # LCEL advanced topics
│   └── 7_Streaming.ipynb           # Streaming responses
│
├── v1/                             # LangChain v1.x tutorials
│   ├── 1.Basics.ipynb              # LangChain v1 basics
│   ├── 2.Messages.ipynb            # Message handling
│   ├── 3.Structured_Outputs.ipynb  # Structured output parsing
│   ├── 4.chain.ipynb               # Building chains
│   ├── 5.chain_with_customRunnable.ipynb  # Custom runnables
│   ├── 6.parallel_chains.ipynb     # Parallel chain execution
│   ├── 7.conditional_chains.ipynb  # Conditional logic in chains
│   │
│   └── ReAct/                      # ReAct agent implementation
│       ├── 1.ReAct_Agnet_intro.ipynb      # ReAct basics
│       ├── 2.ReAct_DB_Agent.ipynb         # SQL database agent
│       ├── init_db.py                      # Database setup
│       ├── demo.py                         # Demo script
│       └── README.md                       # ReAct documentation
│
└── README.md                       # This file
```

## 🎯 Learning Path

### Version 0.3 Track

1. **Introduction** - Get started with LangChain basics and LLM integration
2. **Prompts** - Learn prompt engineering and template management
3. **Chat Memory** - Implement conversation memory and context
4. **Agents Intro** - Understand agent concepts and tool usage
5. **Agent Deep Dive** - Advanced agent patterns and customization
6. **LCEL (Parts 1 & 2)** - Master LangChain Expression Language
7. **Streaming** - Implement real-time streaming responses

### Version 1.x Track

1. **Basics** - Core LangChain v1 concepts and setup
2. **Messages** - Work with different message types
3. **Structured Outputs** - Parse and validate LLM outputs
4. **Chains** - Build and compose simple chains
5. **Custom Runnables** - Create custom runnable components
6. **Parallel Chains** - Execute chains in parallel
7. **Conditional Chains** - Implement branching logic
8. **ReAct Agents** - Build reasoning and acting agents
   - General-purpose agents with multiple tools
   - SQL database query agents

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- A Groq API key (free tier available at [Groq](https://groq.com/))

## 📖 Key Concepts Covered

### Core Components

- **LLMs & Chat Models** - Integration with Groq's LLama models
- **Prompts** - Template creation and management
- **Output Parsers** - Structured output handling
- **Memory** - Conversation history and context management

### Advanced Topics

- **LCEL (LangChain Expression Language)** - Declarative chain composition
- **Agents** - ReAct pattern for reasoning and tool usage
- **Tools** - Web search, Wikipedia, custom tools, SQL databases
- **Streaming** - Real-time response generation
- **Custom Runnables** - Extending LangChain functionality

### Chains

- **Simple Chains** - Basic LLM pipelines
- **Sequential Chains** - Multi-step processing
- **Parallel Chains** - Concurrent execution
- **Conditional Chains** - Dynamic routing and branching

### Agents & Tools

- **ReAct Agents** - Reasoning and acting in a loop
- **Tool Integration** - DuckDuckGo search, Wikipedia
- **SQL Agents** - Natural language database queries
- **Custom Tools** - Building domain-specific tools

## 💡 Example Use Cases

- **Chatbots** - Conversational AI with memory
- **Data Analysis** - Natural language SQL queries
- **Research Assistants** - Multi-tool agents for information gathering
- **Content Generation** - Structured output for articles, summaries
- **Workflow Automation** - Conditional chains for complex tasks

## 🔍 Highlights

### ReAct Agent Project

The `v1/ReAct/` directory contains a complete project demonstrating:

- Multi-tool agent setup (search, Wikipedia, custom tools)
- SQL database agent for sales analytics
- Streaming responses for real-time interaction
- Production-ready code examples

See [v1/ReAct/README.md](v1/ReAct/README.md) for detailed documentation.

## 📚 Resources

- [LangChain Official Documentation](https://python.langchain.com/)
- [Groq API Documentation](https://groq.com/)
- [LangChain Expression Language Guide](https://python.langchain.com/docs/expression_language/)
- [ReAct Paper (Reasoning + Acting)](https://arxiv.org/abs/2210.03629)

**Happy Learning! 🚀**

For questions or issues, refer to the [LangChain documentation](https://python.langchain.com/) or community forums.
