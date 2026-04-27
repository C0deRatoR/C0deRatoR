# Yash Patil

2nd-year B.Tech AI & ML student at Atlas SkillTech, Mumbai.
I build things that ship, like RecSys on 33M records, audio intelligence 
platforms, RAG pipelines, computer vision apps.

---

## Projects

### [StreamLens](https://github.com/C0deRatoR/StreamLens) — Hybrid Movie Recommendation Engine
Context-aware recommendation system on MovieLens (33M ratings · 86k movies · 330k users).  
Three-stage pipeline: TF-IDF content-based filtering, SVD collaborative filtering, configurable hybrid (70/30).  
Evaluated with RMSE, MAE, Precision@K, Recall@K, NDCG@K on 80/20 split.  
FastAPI backend with 8 REST endpoints, TMDB poster caching, 0.08–0.25s response time.

`Python` `FastAPI` `scikit-learn` `SVD` `TF-IDF` `Pandas` `NumPy` `Streamlit`

---

### [Call Analyzer](https://github.com/C0deRatoR/call-analyzer) — AI Audio Intelligence Platform
Upload a call recording, get back a full transcript, speaker breakdown, sentiment timeline, and AI coaching output.  
Whisper transcription at 95%+ accuracy, KeyBERT keyword extraction, VADER + HuggingFace emotion timeline, Gemini coaching.  
Chart.js dashboard with real-time sentiment charts, one-click PDF export via FPDF2.  
pytest + mypy + flake8 CI enforced. Under 2s API response on 100MB audio.

`Python` `Flask` `Whisper` `KeyBERT` `VADER` `HuggingFace` `Gemini API` `Chart.js` `FPDF2`

---

### [DocuChat](https://github.com/C0deRatoR/DocuChat) — RAG Document Q&A
Multi-document RAG pipeline: HuggingFace sentence-transformers + FAISS + LangChain + Gemini.  
Supports PDF, TXT, and DOCX. Source-chunk citations, conversation memory, Dockerised deployment.

`Python` `LangChain` `HuggingFace` `FAISS` `Gemini API` `Streamlit` `Docker`

---

### [VisionTrack](https://github.com/C0deRatoR/VisionTrack) — Real-Time Object Detection
YOLOv8n inference on uploaded images and live webcam feed via Streamlit.  
Confidence threshold slider, class filter, batch processing, exportable annotated results.  
Multi-stage Docker build with 60% image size reduction.

`Python` `YOLOv8` `OpenCV` `Streamlit` `Docker` `Pillow`

---

### [Discord TTS Bot](https://github.com/C0deRatoR/discord-tts-bot) — Neural Voice Cloning
Dual TTS engine (Coqui + ElevenLabs) with CUDA-accelerated neural voice cloning.  
Cold start 2–3s · warmed up ~0.5s · cached phrases under 0.1s.  
Smart async queue, usage analytics, CLI benchmark measuring P50/P95/P99 latency.

`Python` `PyTorch` `discord.py` `Coqui TTS` `ElevenLabs API` `CUDA` `FFmpeg`

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
