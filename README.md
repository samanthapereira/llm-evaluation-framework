# LLM Evaluation Framework

A Python-based framework for evaluating Large Language Model (LLM) applications using DeepEval, with a focus on answer relevancy, faithfulness, and automated AI quality assurance.

## Features

- Answer relevancy evaluation
- Faithfulness and hallucination testing
- Configurable evaluation thresholds
- Jupyter notebooks for developing and validating evaluation scenarios

## Technology Stack

- Python 3.12
- DeepEval
- OpenAI API
- Jupyter Notebook

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/llm-evaluation-framework.git
cd llm-evaluation-framework
```

### 2. Create a virtual environment

```bash
py -3.12 -m venv myenv312
myenv312\Scripts\activate
```

### 3. Install dependencies

```bash
pip install deepeval python-dotenv ipykernel
```

### 4. Configure API keys

Copy `.env.example` to `.env` in the project root.

```dotenv
OPENAI_API_KEY=your_actual_openai_api_key
CONFIDENT_API_KEY=your_actual_confident_ai_api_key
```

The `.env` file is excluded from Git through `.gitignore`. Never commit real API keys.

### 5. Load environment variables

```python
from dotenv import load_dotenv
import os

load_dotenv("../.env", override=True)
```

The relative path assumes the notebook kernel's working directory is `Section1_Intro`.

## Project Structure

```text
llm-evaluation-framework/
├── Section1_Intro/
│   ├── Installation.ipynb
│   └── running-first-test.ipynb
├── .env.example
├── .gitignore
└── README.md
```

## Roadmap

- RAG evaluation using DeepEval and RAGAS
- AI agent and tool-calling evaluation
- Automated evaluation using pytest
- GitHub Actions CI/CD integration
- Evaluation reporting and quality gates

## Security

API credentials are stored locally in `.env` and excluded from version control. No secrets should be hardcoded in notebooks or committed to the repository.
