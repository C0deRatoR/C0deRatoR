# Yash Patil

2nd-year B.Tech AI & ML student at Atlas SkillTech, Mumbai.
I build things that ship, like RecSys on 33M records, audio intelligence
platforms, RAG pipelines, computer vision apps.

Currently: shipping production tools — hiring pipeline, order tracking, admin dashboards — for a manufacturing company.

---

## Open Source Contributions

- [rtk-ai/rtk #2986](https://github.com/rtk-ai/rtk/pull/2986) — Replaced live HTTP calls in the benchmark suite with local fixtures for deterministic, flake-free runs.
- [LobsterTrap/lola #220](https://github.com/LobsterTrap/lola/pull/220) — Added support for `lola.yml` as an alternate module-config filename, preserving `lola.yaml` precedence.
- [dariushoule/x64dbg-automate-pyclient #21](https://github.com/dariushoule/x64dbg-automate-pyclient/pull/21) — Fixed a connection leak: the client now closes its ZMQ connection when a plugin-version handshake fails.
- [livekit/agents #6398](https://github.com/livekit/agents/pull/6398) — Fixed Gemma reasoning-marker tokens leaking into TTS/transcripts/chat history; added a stateful streaming filter that handles markers split across chunks.

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

### [VisionTrack](https://github.com/C0deRatoR/VisionTrack) — Real-Time Object Detection
YOLOv8n inference on uploaded images and live webcam feed via Streamlit.
Confidence threshold slider, class filter, batch processing, exportable annotated results.
Multi-stage Docker build with 60% image size reduction.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-555?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Pillow](https://img.shields.io/badge/Pillow-555?style=flat-square)

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
    "languages"  : ["Python", "SQL", "Java", "Bash"],
    "ml_dl"      : ["scikit-learn", "PyTorch", "XGBoost", "LightGBM", "YOLOv8", "HuggingFace"],
    "genai"      : ["LangChain", "FAISS", "Whisper", "Gemini API", "Ollama"],
    "backend"    : ["FastAPI", "Flask"],
    "devops"     : ["Docker", "Docker Compose", "Linux (Arch)", "Nginx", "Grafana", "Git"],
    "data"       : ["Pandas", "NumPy", "Matplotlib", "Seaborn", "Plotly"],
    "cloud"      : ["Azure", "GCP", "Streamlit Cloud"],
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

## Connect

[LinkedIn](https://linkedin.com/in/yashkpatil) · [Email](mailto:c0derator@proton.me) · [GitHub](https://github.com/C0deRatoR)

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=C0deRatoR&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=C0deRatoR&layout=compact&theme=tokyonight&hide_border=true)
![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=C0deRatoR&theme=tokyonight&hide_border=true)
