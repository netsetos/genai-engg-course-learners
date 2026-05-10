# GenAI Engineering — Learner Code

Companion code repo for the **Netsetos GenAI Engineering** course at [netsetos.com](https://netsetos.com).

> 14 modules · 93 lessons · ~146 hours · production-grade GenAI curriculum

---

## What's in this repo

| Folder | What it contains |
|---|---|
| `module-XX-name/lesson-X.X-slug/notebooks/` | Runnable Colab exercises for the lesson |
| `module-XX-name/lesson-X.X-slug/practice/` | Hands-on coding practice (rolling out over time) |
| `module-XX-name/lesson-X.X-slug/interview/` | Coding interview prep (rolling out over time) |
| `requirements.txt` | Python dependencies |
| `.env.example` | API keys you'll need |

> **Lesson theory, walkthroughs, practice-lab solutions, and interview Q&A live on [netsetos.com](https://netsetos.com).**
> This repo is intentionally **code-only** — open a notebook, run it, modify it, learn by doing.

---

## Getting started

### Option 1 — Colab (recommended)
1. Browse to any lesson's `notebooks/` folder
2. Click the **Open in Colab** badge at the top of the `.ipynb`
3. Set your API keys in Colab (Runtime → Secrets)
4. Run all cells

### Option 2 — Local Jupyter
See [SETUP.md](SETUP.md) for full instructions.

```bash
git clone https://github.com/netsetos/genai-engg-course-learners.git
cd genai-engg-course-learners
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env                # then paste your API keys
jupyter lab
```

---

## Course modules

| # | Module | Lessons |
|---|---|---|
| 00 | Prerequisites | Python for GenAI · Math Foundations |
| 01 | GenAI Foundations | What Is GenAI · History of GenAI |
| 02 | Model Architecture | Tokenization · Transformer · BERT · GPT · Pre-training |
| 03 | Prompt Engineering | Fundamentals · Few-Shot · Reasoning · Context · Tool Use · DSPy · Adversarial |
| 04 | Image & Multimodal | Diffusion · Stable Diffusion · ControlNet · ViT/CLIP · Multimodal · Video/3D · Voice |
| 05 | LLM API Engineering | Multi-Provider · Streaming · Cost · FastAPI · Function Calling · Langfuse |
| 06 | RAG Systems | Fundamentals · Chunking · Embeddings · Retrieval · LangChain · LlamaIndex · GraphRAG · Conversational · Multimodal · Agentic · Evaluation |
| 07 | Fine-Tuning | When · Data Prep · Vertex AI · Open-Source · LoRA/QLoRA · Eval & Deploy |
| 08 | Tool Use & MCP | Function Calling · Schemas · Orchestration · MCP · Servers · Cloud Run · Production |
| 09 | AI Agents | Fundamentals · Architectures · LangGraph · Memory · CrewAI/Agno · Computer Use · Coding · Research · Async · HITL · Eval |
| 10 | Production Deployment | Architecture · Reliability · Gateway · Caching · Docker · CI/CD · Scaling · Monitoring · Incidents · UX |
| 11 | Cost & Performance | Costs · Prompt Optimization · Routing · Latency · Ollama · vLLM/GKE |
| 12 | Ethics & Responsible AI | Bias · Explainability · Copyright · Privacy · Deepfakes · Regulation · Governance |
| 13 | Industry & Capstone | Healthcare · Software Eng · Non-Dev · Capstone Design / Build / Present |

---

## Status — Phase 1

This is the initial code drop:
- ✅ **63 notebooks** ready to run in Colab today
- 🚧 30 lessons' notebooks still being authored — Module 10.2+, all of 11/12/13, and a couple stragglers
- 🚧 `practice/` and `interview/` folders are placeholders — code lands here over time

The `practice/` and `interview/` folders for every lesson are pre-created with a README so you know where things are heading; check back as new content drops.

---

## Need help?

- **Course questions / lesson content:** dashboard at [netsetos.com](https://netsetos.com)
- **Repo issues / typos / broken notebooks:** [open an issue](https://github.com/netsetos/genai-engg-course-learners/issues)
- **Direct contact:** sart@netsetos.com

---

© 2026 Netsetos · Hyderabad, India · All rights reserved
