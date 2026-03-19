# Contributing to DataVyn Labs × Ollama Agents

**A clean, minimal multi-model AI chat workspace powered by Ollama Cloud Models.**  

Live App: [datavyn-labs-x-ollama-agents.streamlit.app](https://datavyn-labs-x-ollama-agents.streamlit.app)

---

Thanks for your interest in contributing! This is a **Python + Streamlit** project by [DataVyn Labs](https://github.com/DataVyn-labs) that lets users chat with 19+ frontier LLMs (OpenAI, DeepSeek, Qwen, Gemini, Mistral, Kimi, GLM, MiniMax, and more) using a **single Ollama Cloud API key** — no separate billing, no credit cards, no extra setup.

When contributing, always keep the core philosophy in mind: **clean, minimal, and fast.**

---

## Table of Contents

- [What This Project Does](#what-this-project-does)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Ways to Contribute](#ways-to-contribute)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Feature Requests](#feature-requests)
- [Code of Conduct](#code-of-conduct)

---

## What This Project Does

- 💬 **Chat with 19+ Ollama Cloud models** from a single UI — OpenAI, DeepSeek, Qwen, Gemini, Mistral, Kimi, GLM, MiniMax, and more.
- 📎 **File uploads** — send `.txt`, `.pdf`, `.json`, `.py`, `.csv` files directly to the model.
- 🎙️ **Voice input** — mic-based input with automatic transcription.
- 🔐 **Secure API key handling** — session-only storage, never written to disk.
- 🌑 **Dark, Claude-style interface** built entirely with Streamlit.

---

## Getting Started

1. **Fork** the repo:  
   → [github.com/anshk1234/DataVyn-Labs-X-Ollama-agents](https://github.com/anshk1234/DataVyn-Labs-X-Ollama-agents)

2. **Clone** your fork:
   ```bash
   git clone https://github.com/<your-username>/DataVyn-Labs-X-Ollama-agents.git
   cd DataVyn-Labs-X-Ollama-agents
   ```

3. **Add the upstream remote:**
   ```bash
   git remote add upstream https://github.com/anshk1234/DataVyn-Labs-X-Ollama-agents.git
   ```

---

## Development Setup

### Prerequisites

- **Python 3.9+**
- An **Ollama Cloud API key** — get one from [ollama.com](https://ollama.com) → Settings → API Keys
- `pip` and optionally `virtualenv`

### Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate       # Windows: venv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure your API key

When the app launches, enter your Ollama Cloud API key directly in the UI — it's stored in session only and never saved to disk. No `.env` file needed.

### Run the app locally

```bash
streamlit run app.py
```

Open your browser at `http://localhost:8501` to see the chat interface.

---

## Ways to Contribute

| Type | Description |
|------|-------------|
| 🐛 Bug Fix | Something broken? Check [open issues](../../issues) for `bug` or `good first issue` tags. |
| 🤖 New Model Support | Add support for a new Ollama Cloud model in the model selector. |
| 📎 File Handling | Improve how uploaded files (`.txt`, `.pdf`, `.json`, `.py`, `.csv`) are processed and sent to the model. |
| 🎙️ Voice Input | Improve mic transcription accuracy or UX. |
| 💅 UI Polish | Small Streamlit UI improvements that stay clean and minimal — layout, spacing, responsiveness. |
| ⚡ Performance | Faster response streaming, reduced re-renders, smarter state management. |
| 📖 Docs | Improve the README, inline comments, or setup instructions. |
| 🧪 Tests | Help add test coverage for core functions. |

> 💡 **For significant changes**, please [open an issue](../../issues/new) first to discuss — this keeps things aligned before you invest time writing code.

---

## Coding Standards

- **Python style:** Follow [PEP 8](https://pep8.org/). Use `black` for formatting:
  ```bash
  black .
  ```
- **Linting:** Use `flake8` to catch issues:
  ```bash
  flake8 .
  ```
- **Streamlit best practices:**
  - Use `st.session_state` correctly — avoid redundant re-renders.
  - Don't persist sensitive data (API keys, user inputs) beyond the session.
  - Keep the UI minimal — don't add widgets or sidebars unless they serve a clear purpose.
- **No hardcoded model names** — use a config list or constant so models can be updated easily.
- **Never commit API keys** or any credentials. Double-check before pushing.

---

## Commit Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short description>
```

### Types

| Type | Use for |
|------|---------|
| `feat` | New feature (e.g. new model, new file type support) |
| `fix` | Bug fix |
| `ui` | Streamlit UI/layout changes |
| `perf` | Performance or streaming improvements |
| `docs` | Documentation only |
| `refactor` | Code cleanup without behavior change |
| `test` | Adding or updating tests |
| `chore` | Deps, config, maintenance |

### Examples

```
feat(models): add MiniMax and GLM support to model selector
fix(upload): handle empty PDF file edge case gracefully
ui(chat): improve message spacing for cleaner Claude-style look
perf(stream): reduce Streamlit re-renders during model streaming
docs: add Ollama API key setup steps to README
```

---

## Pull Request Process

1. **Create a branch** off `main`:
   ```bash
   git checkout -b feat/add-phi4-model-support
   ```

2. **Make focused, atomic commits** — one logical change per commit.

3. **Stay in sync with upstream:**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

4. **Run formatting and linting:**
   ```bash
   black . && flake8 .
   ```

5. **Push and open a PR** against `main`.

6. **In your PR description, include:**
   - What this change does and why
   - Steps to test it locally
   - Which Ollama Cloud model(s) you tested with (e.g. `llama3.2`, `deepseek-r1`, `gemini-2.0-flash`)
   - Screenshots for any UI changes

7. A maintainer will review your PR. Please respond to feedback within a reasonable time — inactive PRs (2+ weeks) may be closed, but feel free to reopen.

---

## Reporting Bugs

[Open a bug report](../../issues/new) and include:

- Clear title describing what's broken
- Steps to reproduce
- Expected vs. actual behavior
- Your environment: OS, Python version, browser, Ollama model used
- Any error messages from the Streamlit terminal or browser console

---

## Feature Requests

[Open a feature request](../../issues/new) with:

- What you want and why it's useful
- How it fits the project's clean, minimal, multi-model chat focus
- Mockups or references if you have them

> Features that add complexity without serving the core chat experience are likely out of scope.

---

## Code of Conduct

Be respectful, constructive, and inclusive. We're building something useful together — keep it collaborative.

---

**Made with ❤️ by [DataVyn Labs](https://github.com/DataVyn-labs) · Powered by Ollama Cloud Models 🚀**
