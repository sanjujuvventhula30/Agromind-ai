# Agromind AI

Agromind AI is a Streamlit-based multi-agent application for agricultural research and agentic workflow experimentation. It includes tools for creating custom agent teams, running research workflows, and generating structured results.

## Features

- Build and save custom agent systems from CSV role-and-instruction data.
- Run multi-agent conversations through OpenRouter.
- Generate, review, and save research articles.
- Use local Hugging Face models with Gemini as a configurable option.
- Persist agent systems and workflow data locally.

## Requirements

- Python 3.10 or later
- Streamlit
- Pandas
- LangChain OpenRouter
- LangChain Core
- LangGraph
- Google Generative AI
- Hugging Face Transformers
- Sentence Transformers
- PyTorch
- DuckDuckGo Search

## Setup

Create and activate a virtual environment:

```powershell
py -m venv agents
agents\Scripts\activate
```

Install the required packages:

```powershell
pip install -U streamlit pandas langchain-openrouter langchain-core langgraph google-generativeai transformers sentence-transformers torch duckduckgo-search
```

## Run the Application

For the agentic system builder:

```powershell
streamlit run drl.py
```

For the research generator:

```powershell
streamlit run aai.py
```

Enter the required API key in the application's sidebar:

- `drl.py` uses an OpenRouter API key.
- `aai.py` uses a Gemini API key.

## Agent CSV Format

Custom systems in `drl.py` require a CSV with these columns:

```csv
Role,Instructions
"Agriculture Expert","Provide practical crop-growing advice."
"Weather Analyst","Interpret available weather forecasts."
```

The project includes `agromind.csv` as an example agent configuration.

## Notes

- API keys are entered through the application and are not stored in source code.
- Local runtime files such as SQLite databases, virtual environments, model caches, and generated workspace files should not be committed.
