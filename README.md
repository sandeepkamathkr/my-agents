# My Agents

A hands-on lab series for exploring Agentic AI using the Anthropic Claude API.

## Setup

1. **Create a virtual environment and install dependencies:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install python-dotenv anthropic
   ```

2. **Add your API key:**
   Create a `.env` file in the project root:
   ```
   ANTHROPIC_API_KEY=your-key-here
   ```

3. **Select the kernel:**
   In IntelliJ IDEA, open the notebook and select `.venv (Python 3.x)` as the kernel.

## Labs

| Notebook | Description |
|----------|-------------|
| [1_lab1.ipynb](1_lab1.ipynb) | Introduction — calling Claude models, asking questions, and rendering responses |

## Requirements

- Python 3.12+
- `anthropic`
- `python-dotenv`
