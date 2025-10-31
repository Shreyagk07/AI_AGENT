# LangChain Tool-Calling Research Agent

This project provides a Python-based research assistant that uses a LangChain agent to answer queries. The agent is empowered with tool-calling capabilities (e.g., web search, Wikipedia) and formats its final answer into a validated Pydantic model.

## ✨ Features

* **Structured Output:** Uses Pydantic to guarantee clean, parseable JSON responses.
* **Tool-Calling:** Built to use external tools to gather live, up-to-date information.
* **Model Agnostic:** Configured to use [OpenRouter](https://openrouter.ai/), allowing easy swapping of LLMs (e.g., DeepSeek, GPT-4o, Claude 3.5 Sonnet) with a single API key.

## 💻 Tech Stack

* **LangChain:** Core framework for agent creation and execution.
* **Pydantic:** For data validation and defining the output schema.
* **OpenRouter:** For LLM API access.
* **python-dotenv:** For managing environment variables.

## 🚀 Quick Start

### 1. Installation

1.  **Clone the repository:**
    

2.  **Create and activate a virtual environment:**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows: .\venv\Scripts\activate
    ```

3.  **Install dependencies:**
    Create a `requirements.txt` file with the following and run `pip install -r requirements.txt`:

    ```ini
    langchain
    langchain-openai
    pydantic
    python-dotenv
    
    # Add libraries for your tools
    # Example:
    # wikipedia
    # tavily-python
    ```

### 2. Configuration

1.  Create a `tools.py` file and define your agent's tools using the `@tool` decorator.
2.  Create a `.env` file in the root directory and add your OpenRouter API key:
    ```
    OPENROUTER_API_KEY="sk-or-v1-..."
    ```

### 3. Run

Execute the main script (e.g., `main.py`) and respond to the prompt:

```sh
python main.py
What can i help you research?****
