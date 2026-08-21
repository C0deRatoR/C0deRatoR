<h1 align="center">Yash Patil</h1>

<p align="center">
  B.Tech CS (AI &amp; ML) · I build things that ship
</p>

<p align="center">
  <code>RAG</code> · <code>Voice Agents</code> · <code>LLM Pipelines</code> · <code>Recommenders</code>
</p>

<p align="center">
  <a href="https://linkedin.com/in/yashkpatil">LinkedIn</a> ·
  <a href="mailto:c0derator@proton.me">Email</a>
</p>

---

## Work

<sub>AI engineering internship · May 2026 – present · the repos are private, so — by capability</sub>

**AI hiring pipeline** — end to end  
Application intake, resume parsing out of object storage, role-specific aptitude banks scored
deterministically, then a Gemini rubric pass: resume/role fit, MCQ, open Q&A, and logistics/culture
as separate sub-scores rather than one opaque number. Experience thresholds gate ranking per role,
an AI-assistance flag routes suspect written answers to human review instead of silently penalising
them, and transient model failures retry on backoff with batch rescoring for anything left pending.
Decision emails then go out on status change — templated, idempotent (never twice), individually
pausable, and replying lands with a human, not a bot.  
`Gemini 2.5 Flash` `Next.js` `Supabase` `Resend` `TypeScript`

**RAG in production**  
Fastify + pgvector retrieval on Voyage AI embeddings, grounded and source-constrained.
Deterministic math kept outside the model — the LLM writes the summary, never the numbers.
Namespace-isolated corpora per product line, review-gated ingestion, retrieval evals.  
`Fastify` `pgvector` `Voyage AI` `Postgres`

**Voice agents**  
Python LiveKit Cloud worker: STT → LLM → TTS, running a structured multi-turn qualification flow.
Endpointing and latency tuning, Hindi/Hinglish handling, region-aware persistence — the worker
POSTs to an API instead of dialling Postgres cross-region.  
`LiveKit` `Deepgram` `Sarvam` `Gemini` `Groq` `ElevenLabs`

**Multimodal extraction**  
Gemini OCR turning photographed cards into structured records, meeting-note extraction, offline
inference as the fallback when OCR misses fields. Document pipelines on scheduled CI.  
`Gemini` `pdfplumber` `Dexie` `GitHub Actions`

**Agentic automation & outreach loops**  
Webhook-driven state machines that qualify before they answer, RAG-backed first-touch replies, and
n8n orchestration. Inbound replies get parsed into structured field diffs a human confirms rather
than free text someone re-types, and an idempotent follow-up scheduler reads reply direction to
nudge at four days, escalate at ten, then mark dormant — guarded on open tasks so a re-run never
double-schedules.  
`n8n` `Playwright` `Fastify` `Webhooks` `Vercel Cron`

> **Guardrails, learned the hard way** — deterministic math separated from generation, auditable
> reference data instead of asking a model for numbers, idempotent upsert-by-UUID sync, and review
> gates on anything ingested.

---

## Projects

**[StreamLens](https://github.com/C0deRatoR/StreamLens)** — hybrid recommender on MovieLens (33M ratings · 86k movies · 330k users)  
TF-IDF content filtering and SVD collaborative filtering in a configurable 70/30 blend, evaluated on
RMSE, MAE, and Precision/Recall/NDCG@K. FastAPI serving in 0.08–0.25s.  
`Python` `FastAPI` `scikit-learn` `Pandas`

**[Call Analyzer](https://github.com/C0deRatoR/call-analyzer)** — upload a call, get back what happened in it  
Transcript, speaker breakdown, sentiment timeline, and coaching notes: Whisper transcription, KeyBERT
keywords, VADER + HuggingFace emotion timeline, Gemini coaching, PDF export. pytest/mypy/flake8 in CI.  
`Python` `Flask` `Whisper` `HuggingFace` `Gemini`

**[AI Interview Coach](https://github.com/C0deRatoR/Ai-InterviewCoach)** — three-agent adaptive mock interviewer  
Six turns; each answer scored on structure, specificity, depth, and communication, and the next
question adapts — probe, redirect, hint, change topic, raise difficulty. Ends with strengths, gaps,
three practice tasks, and one rewritten answer.  
`Python` `FastAPI` `LangChain` `OpenAI` `Next.js`

**[DocuChat](https://github.com/C0deRatoR/DocuChat)** — multi-document RAG over PDF, TXT, and DOCX  
sentence-transformers + FAISS + LangChain + Gemini, with source-chunk citations and conversation
memory. Dockerised.  
`Python` `LangChain` `FAISS` `Gemini` `Docker`

**[Discord TTS Bot](https://github.com/C0deRatoR/discord-tts-bot)** — neural voice cloning on a dual TTS engine  
Coqui + ElevenLabs on CUDA: ~0.5s warmed, under 0.1s cached. Async queue, usage analytics, and a
P50/P95/P99 benchmark CLI.  
`Python` `PyTorch` `Coqui` `ElevenLabs` `CUDA`

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

| | |
|:--|:--|
| **Languages** | `Python` `TypeScript` `SQL` `Bash` |
| **ML/DL** | `PyTorch` `scikit-learn` `HuggingFace` `XGBoost` `YOLOv8` |
| **GenAI** | `LangChain` `pgvector` `FAISS` `Voyage AI` `Gemini` `Claude` `OpenAI` `Ollama` |
| **Voice** | `LiveKit` `Deepgram` `Whisper` `ElevenLabs` `Coqui` |
| **Backend** | `FastAPI` `Fastify` `Flask` `Drizzle` `Prisma` |
| **Web** | `Next.js` `React` `Vite` `Tailwind` |
| **Data** | `Postgres` `Supabase` `Neon` `Pandas` `NumPy` |
| **Infra** | `Docker` `Vercel` `GitHub Actions` `Linux (Arch)` `Nginx` `Grafana` |

---

## Home Lab

Self-hosted server on Proxmox VE — Jellyfin, Nextcloud, Ollama with GPU passthrough, and
Grafana + Prometheus, all containerised behind an Nginx reverse proxy. SSH hardened, 99% uptime.

<br>

<p align="center">
  <sub>AMD × Google Slingshot Hackathon <strong>#10 / 300</strong> · Mastercard Cybersecurity Simulation (Forage) · 5+ AI/ML hackathons</sub>
</p>
