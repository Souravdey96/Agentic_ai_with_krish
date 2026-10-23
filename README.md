# LangChain & Modern Agentic AI Exploration

A structured collection of modern LangChain and LangGraph notebooks demonstrating core LLM integrations, structured outputs, agents, and middleware capabilities.

---

## 📂 Project Structure

```text
├── updated_langchain/
│   ├── langchain_intro.ipynb        # Introduction to LangChain concepts, prompts, and chains
│   ├── modelIntegration.ipynb      # Multi-provider LLM integrations (OpenAI, Google Gemini, Groq)
│   ├── structured_output.ipynb      # Pydantic schemas, typed responses, and function calling
│   └── middleware.ipynb             # Agent middlewares (SummarizationMiddleware, token limits, checkpointers)
├── src/
│   └── krish_projects/              # Python source modules
├── pyproject.toml                   # Project configuration and uv dependencies
├── requirement.txt                  # Exported pip requirements
└── .gitignore                       # Ignored files (secrets, .venv, checkpoints)
```

---

## 🚀 Topics Covered

### 1. `langchain_intro.ipynb`
- Core abstractions: Models, Prompts, Output Parsers.
- Building LCEL (LangChain Expression Language) pipelines.

### 2. `modelIntegration.ipynb`
- Integrating different LLM providers:
  - **OpenAI** (`langchain-openai`)
  - **Google Gemini** (`langchain-google-genai`)
  - **Groq** (`langchain-groq`)
- Handling provider configurations, model switching, and API invocations.

### 3. `structured_output.ipynb`
- Enforcing structured outputs using Pydantic models.
- Handling extraction workflows, data validation, and JSON schemas.

### 4. `middleware.ipynb`
- Modern agent workflows using `create_agent`.
- **SummarizationMiddleware**:
  - Message-based summarization triggers.
  - Token-based summarization triggers and token estimation.
- State persistence using `langgraph.checkpoint.memory.InMemorySaver` and thread IDs.

---

## 🛠️ Setup & Installation

### Prerequisites
- Python 3.13+
- [uv](https://docs.astral.sh/uv/) (recommended) or standard `pip`

### 1. Clone & Set Up Environment

With **uv**:
```bash
uv sync
```

Or with **pip / venv**:
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# Linux/macOS:
source .venv/bin/activate

pip install -r requirement.txt
```

### 2. Configure Environment Variables

Create a `.env` file in the root directory:
```ini
OPENAI_API_KEY="your-openai-api-key"
GOOGLE_API_KEY="your-google-api-key"
GROQ_API_KEY="your-groq-api-key"
```

> **Note:** `.env` is already configured in `.gitignore` to prevent secret leakage.

### 3. Running Notebooks

Launch Jupyter Notebook or open within VS Code:
```bash
jupyter notebook
```
Select the `.venv` kernel when running notebooks.
