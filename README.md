<div align="center">

<!-- HEADER SECTION -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0f23,50:6366f1,100:06b6d4&height=220&section=header&text=Atta%20Ur%20Rehman&fontSize=52&fontColor=f8fafc&fontAlignY=35&desc=AI%20Engineer%20%E2%80%A2%20Building%20Intelligent%20Systems%20That%20Ship&descSize=18&descAlignY=55&animation=fadeIn" width="100%"/>

<br/>

<!-- TAGLINE -->
```
🧠 I don't just build AI models — I build AI systems that run in production.
```

<br/>

<!-- QUICK STATS -->
<img src="https://img.shields.io/badge/Focus-Agentic_AI_&_Multi--Agent_Systems-6366f1?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/Domain-Enterprise_Banking_AI-06b6d4?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/Infra-Local_LLMs_|_Zero_API_Dependency-10b981?style=for-the-badge&logoColor=white" />

<br/><br/>

<!-- ABOUT -->
<table>
<tr>
<td width="100%">

**AI Engineer at Askari Bank** — designing and deploying production-grade Agentic RAG, multi-agent orchestration, and real-time conversational AI for one of Pakistan's largest banks. Every system I build runs on **fully local infrastructure** with zero third-party API dependencies — because in banking, data doesn't leave the building.

I specialize in the hard part: making AI work under **real constraints** — compliance, latency, privacy, and scale.

</td>
</tr>
</table>

</div>

---

## ⚡ What I'm Building Right Now

> *All projects are proprietary production systems at Askari Bank. Architecture details shared; source code is confidential.*

<br/>

### 🏦 Askari Buddy — Enterprise Multi-Domain Banking Assistant
**`Launching on Askari Bank's Mobile App`** &nbsp; `Production` &nbsp; `Multi-Agent` &nbsp; `Voice-Enabled` &nbsp; `Multi-Lingual`

The most comprehensive AI assistant in Pakistani banking — a multi-domain chatbot serving **Islamic Banking, Conventional Banking, Security Operations, and Mobile App Support** through a single intelligent interface.

<table>
<tr>
<td width="50%">

**🏗️ Architecture**
- **Multi-Domain Orchestrator** with intent classification routing to 4 specialized RAG pipelines
- **DomainClassifierAgent** for automatic query routing across Islamic, Conventional, SOC, and App domains
- **Qdrant** vector store with domain-filtered retrieval on a unified collection
- End-to-end **voice pipeline**: Whisper STT → LLM → Edge TTS
- **Multi-lingual** support: English, Urdu, Pashto, Punjabi

</td>
<td width="50%">

**🔧 Stack**
- **Backend:** FastAPI + LangChain + SQLAlchemy + MySQL
- **Frontend:** SvelteKit + TailwindCSS
- **AI:** Ollama (Llama 3.1) + BGE-M3 1024D Embeddings
- **Vector DB:** Qdrant (domain-filtered single collection)
- **Voice:** Whisper STT + Edge TTS
- **Infra:** Docker + Nginx + Supervisor + uv
- **Document Processing:** Tika + Docling

</td>
</tr>
</table>

<details>
<summary>📐 <b>System Architecture (Click to expand)</b></summary>
<br/>

```
Browser → Apache Middleware → Nginx Gateway (SSL) → Reverse Proxy :8005
    └── Askari Buddy Container :8000
          ├── Nginx (API prefix routing)
          └── FastAPI :8181
                ├── MultiDomainOrchestrator
                │     ├── DomainClassifierAgent → Intent Routing
                │     ├── IslamicPipeline       → Shariah-compliant banking RAG
                │     ├── ConventionalPipeline  → Conventional banking RAG
                │     ├── SOCPipeline           → Security operations RAG
                │     └── AppPipeline           → Mobile app support RAG
                ├── Qdrant (askari_buddy collection, domain-filtered)
                ├── Whisper STT ↔ Edge TTS (Voice Pipeline)
                └── MySQL (Users, Conversations, Audit Logs)
```

</details>

<details>
<summary>🔑 <b>Key Features</b></summary>
<br/>

- **JWT Authentication** (HS256) with admin approval workflow, access/refresh token rotation
- **Admin Panel** — User management, FAQ CRUD, cache operations, KB reindexing, audit logs
- **Streaming SSE** chat responses with conversation history persistence
- **Feedback system** — Thumbs up/down on every response for continuous improvement
- **100% local** — No data leaves bank infrastructure. Ever.

</details>

---

### 🕌 Islamic Banking Agentic Bot
**`Production`** &nbsp; `Multi-Agent Orchestration` &nbsp; `Agentic RAG`

<table>
<tr>
<td>

- Orchestrator routes intents to **3 specialized sub-agents**: Document Search, FAQ, and Profit Rates
- **40% improvement** in query resolution efficiency over keyword-based search
- Fully local: **Llama 3.1 + FAISS** — 100% data privacy, zero third-party API calls
- Designed for Shariah-compliance teams who need fast, accurate answers from dense Islamic finance documentation

</td>
</tr>
</table>

---

### 🔒 Information Security BOT — Intelligent Document Analyzer
**`Production`** &nbsp; `Compliance AI` &nbsp; `High-Accuracy Retrieval`

<table>
<tr>
<td>

- Processes **1,285+ compliance requirements** across regulatory frameworks
- **93.4% retrieval accuracy** — achieved by preserving table structures in complex PDFs via **Docling**
- **Sub-1ms query latency** powered by ChromaDB for enterprise-speed document auditing
- Used by IT security teams for real-time compliance verification

</td>
</tr>
</table>

---

### 🎙️ Real-Time Conversational Voice Agent
**`Production`** &nbsp; `Voice AI` &nbsp; `Low-Latency Pipeline`

<table>
<tr>
<td>

- End-to-end **STT → LLM → TTS pipeline** with **< 200ms** total response time
- Dynamic tone and prosody adjustment for natural-sounding conversations
- Designed for banking customers who need hands-free, conversational interactions

</td>
</tr>
</table>

---

### 📊 DataChat — Generative Business Intelligence
**`Production`** &nbsp; `Natural Language Analytics` &nbsp; `Auto-Insight Engine`

<table>
<tr>
<td>

- Natural-language analytics platform: query CSV, Excel, and PDF data conversationally
- **Automated Insight Engine** generates charts, KPI summaries, and trend analysis
- Built for non-technical business users who need data answers without SQL

</td>
</tr>
</table>

---

## 🛠️ Technical Arsenal

<div align="center">

| Domain | Technologies |
|:--|:--|
| **AI/ML Core** | LangChain · CrewAI · Agentic RAG · Multi-Agent Orchestration · Prompt Engineering · NLP · Computer Vision |
| **LLMs** | Ollama · Llama 3.1 · LoRA/QLoRA Fine-tuning · Real-time Voice Pipelines (STT/TTS) · Vapi.ai |
| **Vector & Search** | FAISS · ChromaDB · Qdrant · BGE-M3 Embeddings |
| **ML Frameworks** | PyTorch · TensorFlow · Scikit-learn · Time-Series Forecasting · Statistical Modeling |
| **Backend** | Python · FastAPI · SQLAlchemy · MySQL · SQLite · REST APIs |
| **Frontend** | SvelteKit · Streamlit · TailwindCSS |
| **Data** | Pandas · NumPy · Power BI · EDA · SQL |
| **Infrastructure** | Docker · Nginx · Supervisor · N8n · Zapier · uv |
| **Document AI** | Docling · Tika · Complex PDF Processing |

</div>

---

## 🎯 Impact Numbers

<div align="center">

| Metric | Result |
|:--|:--|
| Query Resolution Efficiency | **↑ 40%** (Islamic Banking Bot) |
| Retrieval Accuracy | **93.4%** (Compliance Document Analyzer) |
| Voice Response Latency | **< 200ms** end-to-end |
| Document Query Latency | **< 1ms** (ChromaDB) |
| Compliance Requirements Processed | **1,285+** |
| Knowledge Domains Served | **4** (Islamic, Conventional, SOC, App) |
| Third-Party API Dependencies | **0** — Fully local infrastructure |
| Languages Supported | **4** (English, Urdu, Pashto, Punjabi) |

</div>

---

## 🎓 Background

**B.S. Artificial Intelligence** — University of Haripur, 2024  
**Data Analytics Digital Bootcamp** — Institute of Emerging Careers, 2025

---

## 📬 Let's Connect

<div align="center">

[![Email](https://img.shields.io/badge/Email-attiqureshi56@gmail.com-6366f1?style=for-the-badge&logo=gmail&logoColor=white)](mailto:attiqureshi56@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-06b6d4?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/)
[![Phone](https://img.shields.io/badge/Phone-+92--316--153--3723-10b981?style=for-the-badge&logo=phone&logoColor=white)]()

</div>

<br/>

<div align="center">

```
"In banking AI, there are no second chances with data privacy.
 Every system I build assumes the worst and delivers the best."
```

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0f23,50:6366f1,100:06b6d4&height=120&section=footer" width="100%"/>
