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

## Notes

### Lab 1 — Key Concepts

**Environment Setup**
- Use a `.venv` virtual environment and store API keys in a `.env` file (never hardcode them)

**Anthropic SDK Basics**
- Create a client: `anthropic.Anthropic()`
- Make API calls: `client.messages.create(model=..., max_tokens=..., messages=...)`
- Model selection: `claude-haiku` (fast/cheap) vs `claude-sonnet` (more powerful)

**Messages Format**
- Conversations are structured as a list of dicts: `[{"role": "user", "content": "..."}]`
- This is the core primitive for all LLM interactions

**Multi-Step LLM Chaining**
- The output of one LLM call becomes the input to the next
- Example: pick a business area → identify a pain point → propose an agentic solution
- This sequential chaining pattern is the foundation of agentic AI systems

**IntelliJ Tip**
- `display(Markdown(answer))` may not render in IntelliJ — use `Markdown(answer)` as the last line in a cell, or `print(answer)` for plain text

## Requirements

- Python 3.12+
- `anthropic`
- `python-dotenv`
