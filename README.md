# Multi-AI Orchestrator

Minimal Streamlit app that orchestrates multiple LLMs in a sequential pipeline using CrewAI.

## Features
- Simple Streamlit UI (`app.py`) to provide a single prompt and run a multi-agent pipeline
- Agents: ChatGPT (OpenAI), Claude (Anthropic), Perplexity, Gemini (Google)

## Setup
1. Create a Python virtual environment and activate it.
2. Install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

3. Run the app:

```bash
streamlit run app.py
```

4. Enter your API keys in the Streamlit sidebar (OpenAI, Anthropic, Google, Perplexity).

## Publish to GitHub
1. Initialize git (if not already):

```bash
git init
git add .
git commit -m "Initial commit: Multi-AI Orchestrator"
```

2. Create a remote repository on GitHub (via website or `gh` CLI), then push:

```bash
# with gh CLI
gh repo create my-org/multi-ai-orchestrator --public --source=. --remote=origin
git push -u origin main

# or using manual remote
git remote add origin https://github.com/<your-username>/<repo>.git
git branch -M main
git push -u origin main
```

## Notes
- The project uses `crewai` and platform-specific SDKs. Ensure the required SDK packages and credentials are available in your environment.
- Consider adding a `.env` or GitHub Secrets for CI if you automate deployments. Never commit API keys.
