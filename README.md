# Agentic Patterns

A comprehensive collection of agentic design patterns using LangChain and LangGraph. This repository demonstrates both single-agent and multi-agent architectures with practical, hands-on examples in Jupyter notebooks.

## 📋 Purpose

This repository serves as a learning resource and reference implementation for various agentic patterns in AI development. It explores different approaches to building autonomous AI agents that can:

- Make decisions independently
- Use tools and external functions
- Work collaboratively in multi-agent systems
- Generate structured outputs
- Chain operations for complex workflows

Whether you're building a simple chatbot or a complex multi-agent system, these patterns provide foundational building blocks for creating robust AI applications.

## 📂 Repository Contents

### Single-Agentic Patterns

Located in `single-agentic-patterns/`, these notebooks demonstrate fundamental patterns for individual agents:

- **[tool_calling.ipynb](single-agentic-patterns/tool_calling.ipynb)**: Demonstrates how agents can interact with external tools and functions using LangChain's `@tool` decorator and LangGraph's `ToolNode`. Covers the complete LLM → tools → LLM cycle.

- **[structured_output.ipynb](single-agentic-patterns/structured_output.ipynb)**: Shows how to constrain agent outputs into structured formats, enabling reliable data extraction and consistent response formatting.

### Multi-Agentic Patterns

Located in `multi-agentic-patterns/`, these notebooks explore patterns for coordinating multiple agents:

- **[prompt-chaininig.ipynb](multi-agentic-patterns/prompt-chaininig.ipynb)**: Implements sequential agent collaboration where multiple agents work on a task in sequence (e.g., Extractor → Reviewer). Each agent's output becomes the next agent's input, forming a processing pipeline.

- **[supervisor.ipynb](multi-agentic-patterns/supervisor.ipynb)**: Demonstrates the Supervisor pattern where a central supervisor agent routes tasks to specialized worker agents. The supervisor analyzes incoming queries and delegates work appropriately, managing all user interactions.

**Note**: The repository is likely to be extended so the contents might change a little through time

## 🚀 Installation

### Prerequisites

- Python 3.12 or higher
- uv package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/Dybal-Ilia/agentic-patterns.git
   cd agentic-patterns
   ```

2. **Create a virtual environment (using uv)**
   ```bash
   uv venv
   ```

3. **Install dependencies (using uv)**
   
   ```bash
   uv sync
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the root directory and add your API keys:
   
   You can look up for required keys in [.env.example](.env.example) or in case of usage different from examples providers you can pass your own provider API keys
   

5. **Launch Notebooks**

   In case you want to experiment with notebooks, feel free to launch any of them
   
   Navigate to the desired notebook in either `single-agentic-patterns/` or `multi-agentic-patterns/` directories.

## 📦 Dependencies

This project uses the following key libraries:

- **langchain** (>=1.2.7): Framework for building LLM applications
- **langchain-groq** (>=1.1.2): Groq integration for LangChain
- **langgraph** (>=1.0.7): Library for building stateful, multi-agent workflows
- **python-dotenv** (>=1.2.1): Environment variable management
- **ipykernel** (>=7.1.0): Jupyter notebook support

For a complete list of dependencies, see [pyproject.toml](pyproject.toml).

**Note**: the repository is likely to be extended so additional API keys might be required through time

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Add new agentic patterns
- Improve existing examples
- Fix bugs or typos
- Enhance documentation

## 📝 License

This project is provided as-is for educational purposes.

## 🔗 Resources

- [LangChain Documentation](https://python.langchain.com/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [Groq API](https://groq.com/)

---

**Note**: Remember to keep your API keys secure and never commit them to version control.