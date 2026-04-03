# Hey, I'm Yash 👋

**AI/ML Developer · Mumbai, India**

2nd-year B.Tech student in CS with AI & ML at Atlas SkillTech University. I build things that actually work — end-to-end ML pipelines, NLP platforms, computer vision apps, and self-hosted infrastructure. I care about shipping real projects, not just collecting tutorials.

---

## 🛠️ What I Build With

```python
stack = {
    "languages"  : ["Python", "SQL", "JavaScript", "Bash"],
    "ml_dl"      : ["scikit-learn", "PyTorch", "YOLOv8", "HuggingFace Transformers"],
    "nlp_audio"  : ["OpenAI Whisper", "KeyBERT", "VADER", "Google Gemini API"],
    "backend"    : ["FastAPI", "Flask"],
    "devops"     : ["Docker", "Docker Compose", "Linux", "Nginx", "Git"],
    "data"       : ["Pandas", "NumPy", "Matplotlib"],
    "tools"      : ["Streamlit", "Jupyter", "FFmpeg", "Grafana"],
    "learning"   : ["LangChain", "Deep Learning", "Proxmox", "Ollama"],
}
```

---

## 🚀 Projects

### 🎬 [StreamLens](https://github.com/C0deRatoR/StreamLens) — Hybrid Movie Recommendation Engine
> Context-aware recommendation system on the MovieLens dataset (33M ratings · 86k movies · 330k users)

- **3 ML models**: TF-IDF Content-Based · SVD Collaborative Filtering · Configurable Hybrid (70/30)
- **Evaluated** with RMSE, MAE, Precision@K, Recall@K, NDCG@K on 80/20 split
- **FastAPI** backend with 8 REST endpoints + TMDB poster caching · **~0.08–0.25s** response time
- **Streamlit** frontend with context sidebar, match-score bars, and paginated movie cards

`Python` `FastAPI` `scikit-learn` `SVD` `TF-IDF` `Pandas` `NumPy` `Streamlit`

---

### 🎧 [Call Analyzer](https://github.com/C0deRatoR/call-analyzer) — AI Audio Intelligence Platform
> Upload a call recording → get transcription, speaker breakdown, sentiment timeline, and AI coaching

- **OpenAI Whisper** transcription (95%+ accuracy) + **Speaker Diarization** via pause heuristics
- **KeyBERT** keyword extraction · **VADER + HuggingFace** emotion timeline · **Gemini** coaching advice
- **Chart.js** glassmorphism dashboard with real-time sentiment charts · one-click **FPDF2** PDF reports
- Enforced **pytest + mypy + flake8** CI pipeline · **<2s** API response on 100MB audio files

`Python` `Flask` `Whisper` `KeyBERT` `VADER` `HuggingFace` `Gemini API` `Chart.js` `FPDF2`

---

### 🎯 [VisionTrack](https://github.com/C0deRatoR) — Real-Time Object Detection *(In Progress)*
> YOLOv8-powered web app for real-time detection on images and webcam feed

- Bounding boxes, class labels, confidence scores rendered live
- Containerised with **Docker** for one-command deployment

`Python` `YOLOv8` `OpenCV` `Streamlit` `Docker`

---

### 🤖 [Discord TTS Bot](https://github.com/C0deRatoR/discord-tts-bot) — Voice Cloning & Synthesis
> Dual TTS engine (Coqui + ElevenLabs) with GPU-accelerated voice cloning for Discord

- Cold start: **2–3s** · Warmed up: **~0.5s** · Cached phrases: **<0.1s**
- Smart queue, admin controls, voice backup/restore, usage analytics

`Python` `PyTorch` `discord.py` `Coqui TTS` `ElevenLabs API` `CUDA`

---

## 🏠 Home Lab

Running a self-hosted Linux server on **Proxmox VE**:

| Service | Purpose |
|---|---|
| 🎬 **Jellyfin** | Media server |
| 🎵 **FLAC Library** | Hi-fi audio collection |
| ☁️ **Nextcloud** | Personal cloud storage |
| 🧠 **Ollama** | Local LLM inference |
| 📊 **Grafana + Prometheus** | Resource monitoring |

All containerised with Docker Compose · Nginx reverse proxy · SSH hardening

---

## 📊 Stats

![Yash's GitHub Stats](https://github-readme-stats.vercel.app/api?username=C0deRatoR&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=C0deRatoR&layout=compact&theme=tokyonight&hide_border=true)

---

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-yashkpatil-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/yashkpatil)
[![Email](https://img.shields.io/badge/Email-c0derator@proton.me-8B5CF6?style=flat&logo=protonmail)](mailto:c0derator@proton.me)

---

*Currently seeking AI/ML internships in Mumbai · Summer 2025*
