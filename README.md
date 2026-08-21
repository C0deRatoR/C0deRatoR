# Yash Patil

B.Tech CS (AI & ML) student.
I build things that ship, like RecSys on 33M records, audio intelligence
platforms, RAG pipelines, computer vision apps.

Currently: an AI engineering internship — shipping production RAG, voice agents, and LLM scoring pipelines.

---

## Production AI Work

A year of internship work. The repos are private, so this is what I actually built, by capability.

**RAG in production**
Fastify + pgvector retrieval API with Voyage AI embeddings and grounded, source-constrained answers.
Deterministic math kept *outside* the model — the LLM writes the summary, never the numbers.
Namespace-isolated corpora for two separate product lines. Review-gated ingestion of a scraped corpus. Eval scripting for retrieval quality.

**Voice agents**
Python LiveKit Cloud worker: Deepgram/Sarvam STT → Gemini/Groq LLM → ElevenLabs TTS, driving a structured multi-turn qualification flow.
STT endpointing and latency tuning (`endpointing_ms` sweeps, provider normalisation, transcript-preview logging), Hindi/Hinglish handling.
Region-aware persistence — the worker POSTs to an API instead of dialling Postgres cross-region.

**LLM scoring & evaluation**
Applicant scoring 0–100 across five dimensions, role-specific question banks, experience-gated ranking, automated decision flows behind explicit guards.

**Multimodal extraction**
Gemini OCR turning photographed cards into structured records, plus meeting-note extraction, with conservative offline inference as the fallback when OCR misses fields.
Deepgram voice-note capture. `pdfplumber` + `reportlab` document pipelines running on scheduled CI.

**Agentic automation**
Webhook-driven state machines that qualify before they answer, RAG-backed first-touch replies, n8n workflow orchestration, Playwright scraping for corpus building.

**Guardrails, learned the hard way**
Deterministic math separated from generation. Auditable reference data (central-bank FX) instead of asking a model for numbers.
Idempotent upsert-by-UUID sync RPCs. Review gates on anything ingested. Disposable QA data deleted after verification.

---

## Projects

### [StreamLens](https://github.com/C0deRatoR/StreamLens) — Hybrid Movie Recommendation Engine
Context-aware recommendation system on MovieLens (33M ratings · 86k movies · 330k users).
Three-stage pipeline: TF-IDF content-based filtering, SVD collaborative filtering, configurable hybrid (70/30).
Evaluated with RMSE, MAE, Precision@K, Recall@K, NDCG@K on 80/20 split.
FastAPI backend with 8 REST endpoints, TMDB poster caching, 0.08–0.25s response time.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![SVD](https://img.shields.io/badge/SVD-555?style=flat-square)
![TF--IDF](https://img.shields.io/badge/TF--IDF-555?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

---

### [Call Analyzer](https://github.com/C0deRatoR/call-analyzer) — AI Audio Intelligence Platform
Upload a call recording, get back a full transcript, speaker breakdown, sentiment timeline, and AI coaching output.
Whisper transcription at 95%+ accuracy, KeyBERT keyword extraction, VADER + HuggingFace emotion timeline, Gemini coaching.
Chart.js dashboard with real-time sentiment charts, one-click PDF export via FPDF2.
pytest + mypy + flake8 CI enforced. Under 2s API response on 100MB audio.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat-square&logo=openai&logoColor=white)
![KeyBERT](https://img.shields.io/badge/KeyBERT-555?style=flat-square)
![VADER](https://img.shields.io/badge/VADER-555?style=flat-square)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Gemini API](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)
![FPDF2](https://img.shields.io/badge/FPDF2-555?style=flat-square)

---

### [AI Interview Coach](https://github.com/C0deRatoR/Ai-InterviewCoach) — Adaptive Three-Agent Mock Interviewer
Enter a target role, optional background, and a focus area (behavioural, technical, case, or mixed); the coach runs a six-turn interview.
Each answer is scored on structure, specificity, depth, and communication, and the next question adapts — probe, redirect, hint, change topic, or raise difficulty.
Ends with strengths, gaps, three practice tasks, and one rewritten answer.
Ships both a Next.js web interface and a CLI, with a `unittest` suite over the orchestration controller.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenAI API](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

---

### [DocuChat](https://github.com/C0deRatoR/DocuChat) — RAG Document Q&A
Multi-document RAG pipeline: HuggingFace sentence-transformers + FAISS + LangChain + Gemini.
Supports PDF, TXT, and DOCX. Source-chunk citations, conversation memory, Dockerised deployment.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![FAISS](https://img.shields.io/badge/FAISS-555?style=flat-square)
![Gemini API](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

### [Discord TTS Bot](https://github.com/C0deRatoR/discord-tts-bot) — Neural Voice Cloning
Dual TTS engine (Coqui + ElevenLabs) with CUDA-accelerated neural voice cloning.
Cold start 2–3s · warmed up ~0.5s · cached phrases under 0.1s.
Smart async queue, usage analytics, CLI benchmark measuring P50/P95/P99 latency.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![discord.py](https://img.shields.io/badge/discord.py-5865F2?style=flat-square&logo=discord&logoColor=white)
![Coqui TTS](https://img.shields.io/badge/Coqui_TTS-555?style=flat-square)
![ElevenLabs API](https://img.shields.io/badge/ElevenLabs_API-555?style=flat-square)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

---

## Stack

```python
stack = {
    "languages"  : ["Python", "TypeScript", "SQL", "Java", "Bash"],
    "ml_dl"      : ["scikit-learn", "PyTorch", "XGBoost", "LightGBM", "YOLOv8", "HuggingFace"],
    "genai"      : ["LangChain", "pgvector", "FAISS", "Voyage AI", "Whisper",
                    "Gemini API", "Claude API", "OpenAI API", "Groq", "Ollama"],
    "voice"      : ["LiveKit", "Deepgram", "Sarvam", "ElevenLabs", "Coqui TTS"],
    "backend"    : ["FastAPI", "Flask", "Fastify", "Drizzle", "Prisma"],
    "web"        : ["Next.js", "React", "Vite", "Tailwind", "PWA / offline (Dexie)"],
    "data"       : ["Postgres", "Supabase", "Neon", "Pandas", "NumPy", "Matplotlib", "Plotly"],
    "testing"    : ["pytest", "Vitest", "Playwright", "mypy", "ruff"],
    "devops"     : ["Docker", "Docker Compose", "Vercel", "GitHub Actions", "n8n",
                    "Linux (Arch)", "Nginx", "Grafana", "Git"],
    "cloud"      : ["Azure", "GCP", "AWS (S3, Textract, Comprehend)"],
}
```

---

## Home Lab

Self-hosted Linux server on Proxmox VE. All services containerised with Docker Compose behind an Nginx reverse proxy.

| Service | Purpose |
|---|---|
| Jellyfin | Media server |
| Nextcloud | Personal cloud storage |
| Ollama | Local LLM inference (GPU passthrough) |
| Grafana + Prometheus | Resource monitoring |

SSH hardened · 99% uptime across 4+ concurrent services.

---

## Certifications

- AMD x Google Slingshot Hackathon — **#10 / 300**
- Mastercard Cybersecurity Simulation · Forage
- 5+ AI/ML Hackathons · Devpost

---

## Open Source

Merged fixes upstream in [livekit/agents](https://github.com/livekit/agents/pull/6398),
[pipecat](https://github.com/pipecat-ai/pipecat/pull/5027),
[langwatch/scenario](https://github.com/langwatch/scenario/pull/841),
[lola](https://github.com/LobsterTrap/lola/pull/220), and
[CodeGraphContext](https://github.com/CodeGraphContext/CodeGraphContext/pull/1643)
([×2](https://github.com/CodeGraphContext/CodeGraphContext/pull/1540)) — mostly small correctness
bugs in LLM/voice pipelines and code-graph parsers.

---

## Connect

[LinkedIn](https://linkedin.com/in/yashkpatil) · [Email](mailto:c0derator@proton.me) · [GitHub](https://github.com/C0deRatoR)

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=C0deRatoR&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=C0deRatoR&layout=compact&theme=tokyonight&hide_border=true)
![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=C0deRatoR&theme=tokyonight&hide_border=true)
