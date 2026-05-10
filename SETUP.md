# Setup

Two ways to run the notebooks: **Colab** (zero install) or **local Jupyter** (full control). Both work — Colab is the fastest path for most learners.

---

## Option 1 — Google Colab (recommended)

1. Open any notebook on GitHub (e.g. `module-01-genai-foundations/lesson-1.1-what-is-genai/notebooks/exercises-1.1.ipynb`)
2. Click the **Open in Colab** badge at the top
3. Add your API keys to Colab:
   - Click the 🔑 key icon in the left sidebar
   - Add: `ANTHROPIC_API_KEY`, `OPENAI_API_KEY`, etc. (only the ones the lesson needs)
   - Toggle "Notebook access" ON
4. Runtime → Run all

In your notebook, retrieve a key with:
```python
from google.colab import userdata
import os
os.environ["ANTHROPIC_API_KEY"] = userdata.get("ANTHROPIC_API_KEY")
```

**Free Colab tier is enough for 90% of the course.** A few lessons (fine-tuning in module 7, image generation in module 4) benefit from Colab Pro's GPU.

---

## Option 2 — Local Jupyter

### Prerequisites
- Python **3.11+** (3.10 will work but 3.11 is the target)
- pip
- ~2 GB free disk for dependencies (more if you run module 4 image lessons)

### Steps

```bash
# Clone
git clone https://github.com/netsetos/genai-engg-course-learners.git
cd genai-engg-course-learners

# Virtual environment
python -m venv .venv
source .venv/bin/activate          # Windows PowerShell: .venv\Scripts\Activate.ps1
                                   # Windows Cmd:        .venv\Scripts\activate.bat

# Install base dependencies
pip install -r requirements.txt

# API keys
cp .env.example .env
# Edit .env in your editor and paste your API keys

# Launch Jupyter
jupyter lab
```

Then open any notebook and run it. Each notebook's first code cell loads `.env` automatically:
```python
from dotenv import load_dotenv
load_dotenv()
```

---

## API keys you'll need

The course uses several LLM providers. **You don't need all keys at once** — only for the lessons you're running.

| Key | Used in | Where to get it |
|---|---|---|
| `ANTHROPIC_API_KEY` | Most lessons (Claude is the primary LLM) | [console.anthropic.com](https://console.anthropic.com) |
| `OPENAI_API_KEY` | Modules 5, 8, 9 | [platform.openai.com](https://platform.openai.com) |
| `GOOGLE_API_KEY` | Modules 4, 7 (Gemini) | [aistudio.google.com](https://aistudio.google.com) |
| `LANGFUSE_PUBLIC_KEY`, `LANGFUSE_SECRET_KEY` | Lesson 5.6 (observability) | [cloud.langfuse.com](https://cloud.langfuse.com) |
| `PINECONE_API_KEY` | Module 6 (optional — Chroma works locally) | [pinecone.io](https://pinecone.io) |
| `HF_TOKEN` | Modules 4, 7 (gated models) | [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens) |

> **Anthropic gives ~$5 free credit** when you sign up — enough to do most of modules 1-9 if you're frugal with prompt sizes.

---

## Lesson-specific extras

Some lessons install extra packages in their first cell (e.g., `diffusers`, `transformers`, `langgraph`, `ragas`, `langfuse`, `crewai`). These aren't in the base `requirements.txt` because they're large or only needed for one lesson — let the notebook install them on first run.

---

## Common errors

**`ANTHROPIC_API_KEY not set`**
- Local: check `.env` file has the key, no quotes around the value
- Colab: check the secret name matches exactly, "Notebook access" toggle is ON

**`429 Rate limit exceeded`**
- Wait 60 seconds and retry
- Reduce request volume in the cell
- Upgrade your provider tier

**`ModuleNotFoundError: No module named 'X'`**
- `pip install X` (or re-run the notebook's install cell)
- If working locally, make sure your virtual environment is activated

**`CUDA out of memory` (GPU lessons)**
- Restart the runtime (Colab) or kernel (local)
- Use smaller batch size in the notebook
- Switch to CPU (slower but works) by setting `device = "cpu"`

**Notebook won't open in Colab**
- The repo must be public for Colab badges to work without auth (this repo is public ✓)
- If still broken, try opening Colab → File → Open notebook → GitHub tab → paste the URL

---

## Need help?

[Open an issue](https://github.com/netsetos/genai-engg-course-learners/issues) with:
- Which lesson and notebook
- Error message (full traceback)
- Whether you're on Colab or local, OS, Python version
