# Yash Patil

B.Tech CS (AI & ML) student. I build things that ship — RAG pipelines, voice agents,
recommender systems, audio intelligence.

<sub>[LinkedIn](https://linkedin.com/in/yashkpatil) · [Email](mailto:c0derator@proton.me)</sub>

---

## Work

AI engineering internship, May 2026 – present. The repos are private, so — by capability:

**RAG in production**
Fastify + pgvector retrieval API on Voyage AI embeddings, grounded and source-constrained.
Deterministic math kept outside the model — the LLM writes the summary, never the numbers.
Namespace-isolated corpora per product line, review-gated ingestion, retrieval evals.

**Voice agents**
Python LiveKit Cloud worker: Deepgram/Sarvam STT → Gemini/Groq → ElevenLabs TTS, running a
structured multi-turn qualification flow. Endpointing and latency tuning, Hindi/Hinglish handling,
region-aware persistence (the worker POSTs to an API instead of dialling Postgres cross-region).

**LLM scoring**
Applicant scoring 0–100 across five dimensions, role-specific question banks, experience-gated
ranking, automated decisions behind explicit guards.

**Multimodal extraction**
Gemini OCR turning photographed cards into structured records, meeting-note extraction, offline
inference as the fallback when OCR misses fields. `pdfplumber` document pipelines on scheduled CI.

**Agentic automation**
Webhook-driven state machines that qualify before they answer, RAG-backed first-touch replies,
n8n orchestration, Playwright scraping for corpus building.

**Guardrails, learned the hard way**
Deterministic math separated from generation. Auditable reference data instead of asking a model
for numbers. Idempotent upsert-by-UUID sync. Review gates on anything ingested.

---

## Projects

**[StreamLens](https://github.com/C0deRatoR/StreamLens)** — hybrid recommender on MovieLens (33M ratings, 86k movies, 330k users).
TF-IDF content filtering + SVD collaborative filtering in a configurable 70/30 blend, evaluated on RMSE, MAE, and Precision/Recall/NDCG@K. FastAPI serving in 0.08–0.25s.
<sub>Python · FastAPI · scikit-learn · Pandas</sub>

**[Call Analyzer](https://github.com/C0deRatoR/call-analyzer)** — upload a call, get a transcript, speaker breakdown, sentiment timeline, and coaching notes.
Whisper transcription, KeyBERT keywords, VADER + HuggingFace emotion timeline, Gemini coaching, PDF export. pytest/mypy/flake8 in CI.
<sub>Python · Flask · Whisper · HuggingFace · Gemini</sub>

**[AI Interview Coach](https://github.com/C0deRatoR/Ai-InterviewCoach)** — three-agent adaptive mock interviewer.
Six turns, each answer scored on structure, specificity, depth, and communication; the next question adapts — probe, redirect, hint, change topic, raise difficulty. Ends with strengths, gaps, three practice tasks, one rewritten answer.
<sub>Python · FastAPI · LangChain · OpenAI · Next.js</sub>

**[DocuChat](https://github.com/C0deRatoR/DocuChat)** — multi-document RAG over PDF, TXT, and DOCX.
sentence-transformers + FAISS + LangChain + Gemini, with source-chunk citations and conversation memory. Dockerised.
<sub>Python · LangChain · FAISS · Gemini · Docker</sub>

**[Discord TTS Bot](https://github.com/C0deRatoR/discord-tts-bot)** — neural voice cloning with a dual TTS engine.
Coqui + ElevenLabs on CUDA: ~0.5s warmed, under 0.1s cached. Async queue, usage analytics, P50/P95/P99 benchmark CLI.
<sub>Python · PyTorch · Coqui · ElevenLabs · CUDA</sub>

---

## Open Source

Merged fixes upstream in [livekit/agents](https://github.com/livekit/agents/pull/6398),
[pipecat](https://github.com/pipecat-ai/pipecat/pull/5027),
[langwatch/scenario](https://github.com/langwatch/scenario/pull/841),
[lola](https://github.com/LobsterTrap/lola/pull/220), and
[CodeGraphContext](https://github.com/CodeGraphContext/CodeGraphContext/pull/1643)
([×2](https://github.com/CodeGraphContext/CodeGraphContext/pull/1540)) — correctness bugs in
LLM/voice pipelines and code-graph parsers.

---

## Stack

- **Languages** — Python · TypeScript · SQL · Bash
- **ML/DL** — PyTorch · scikit-learn · HuggingFace · XGBoost · YOLOv8
- **GenAI** — LangChain · pgvector · FAISS · Voyage AI · Gemini · Claude · OpenAI · Ollama
- **Voice** — LiveKit · Deepgram · Whisper · ElevenLabs · Coqui
- **Backend** — FastAPI · Fastify · Flask · Drizzle · Prisma
- **Web** — Next.js · React · Vite · Tailwind
- **Data** — Postgres · Supabase · Neon · Pandas · NumPy
- **Infra** — Docker · Vercel · GitHub Actions · Linux (Arch) · Nginx · Grafana

---

## Home Lab

Self-hosted server on Proxmox VE — Jellyfin, Nextcloud, Ollama with GPU passthrough, and
Grafana + Prometheus, all containerised behind an Nginx reverse proxy. SSH hardened, 99% uptime.

---

## Elsewhere

AMD × Google Slingshot Hackathon — **#10 / 300** · Mastercard Cybersecurity Simulation (Forage) · 5+ AI/ML hackathons
