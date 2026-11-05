# 👋 Hi, I'm Matheus

**AI/ML Engineer based in Porto, Portugal.** I build LLM applications and ML systems, and I own what happens after the demo: evaluation, security, observability, CI/CD and compliance.

Today I run a multilingual GenAI chatbot in production at Living Tours, from architecture to deployment. My full-stack background (Next.js, React, TypeScript) means I can take a model all the way to a product people actually use.

**What I work on:** RAG · Agentic AI & MCP · LLM evaluation & guardrails · LLM fine-tuning · MLOps

📍 **Open to AI/ML Engineer roles:** hybrid in Porto or remote.

---

## 🌟 Professional Experience

### AI & Web Developer @ Living Tours
*Porto, Portugal · May 2025 – Present*

I own the full lifecycle of the Living Cruise GenAI chatbot, running in production in four languages (PT/EN/ES/FR).

- **Architecture:** led the migration from AWS Lambda + Groq to Cloudflare Workers, Containers and Workers AI, with a FastAPI (Python 3.13) and PostgreSQL backend
- **Reliability:** grew a property-based regression eval suite from 9 to 20 test cases, fixing hallucination and off-topic failures
- **Security:** built a three-layer prompt injection defense and PII masking, including in Langfuse traces
- **Compliance:** implemented EU AI Act Article 50 transparency requirements
- **Delivery:** set up GitHub Actions CI/CD with automated checks, a production approval gate and post-deploy smoke tests
- **Scale-out:** designed a multi-site architecture that serves a second brand with isolated storage and secrets

### AI/ML Engineer & Web Developer @ Crunch Equation
*Vila Nova de Gaia, Portugal · Nov 2024 – Dec 2025*

- Built RAG chatbots with LangChain and ChromaDB, and led internal chatbot development
- Fine-tuned Llama 3.2 3B with QLoRA
- Developed full-stack applications with Next.js, React and TypeScript on AWS, Azure and GCP

---

## 🎯 Featured Projects

### 🏨 hotelml: End-to-End MLOps Platform
**MLOps / LLMOps** | *Personal Project* | 🚧 *In active development*

A reference platform for the full ML production lifecycle, using hotel booking cancellation prediction as the use case. The focus is on operating a model safely, not just training one.

**Tech Stack**: Python, scikit-learn, MLflow, GitHub Actions, pytest, mypy, ruff

**Built so far**:
- **Safe releases:** champion/challenger model registry with conditional promotion, plus rollback that needs no rebuild or redeploy
- **Trustworthy evaluation:** temporal train/test split, with leakage columns removed and a test guarding against their return
- **Serving-ready models:** feature engineering lives inside the registered pipeline, so the model accepts raw request payloads
- **Data contracts:** schema validation that fails early and reports every problem at once
- **Secure deserialization:** an explicit skops allowlist instead of disabling MLflow's safety check
- **Engineering quality:** CI with lint, type checks and an 80% coverage gate (25 tests, 96% coverage), plus Architecture Decision Records

**Roadmap**:

| Phase | Scope | Status |
|---|---|---|
| 1 | Packaging, tests, CI, MLflow training, model registry | ✅ Done |
| 2 | FastAPI + Docker, Terraform on Azure, CD | Planned |
| 3 | Feature pipeline and batch scoring with PySpark | Planned |
| 4 | Drift and quality monitoring, alerts, SLOs, runbooks, automated retraining | Planned |
| 5 | LLMOps with the Anthropic API: tracing, evals, versioned prompts, guardrails, cost control | Planned |
| 6 | Simulated post-mortem, reusable template, architecture diagram | Planned |

---

### 🎙️ Jarvis: Personal Voice Assistant
**Voice AI / Agentic AI** | *Personal Project* | 🚧 *In active development*

An Iron Man-style voice assistant: a double clap wakes it up, it listens, reasons, uses tools and answers out loud. It is designed around the real constraints of voice agents: latency, cost and safe actions.

**Tech Stack**: Python, Anthropic API, MCP, faster-whisper, ElevenLabs, Telegram Bot API

**Design highlights**:
- **Custom agent core** on the Anthropic SDK, with tools exposed through MCP servers so the model and the tools can change independently
- **Low-latency pipeline:** local speech-to-text with faster-whisper and streaming text-to-speech with ElevenLabs Flash
- **Cost-aware model routing:** Claude Haiku by default for the voice loop, Claude Sonnet only for tasks that need deeper reasoning
- **Human in the loop:** Jarvis drafts emails, but nothing is sent until I confirm by voice
- **Multi-agent development:** Claude Code and Codex share project memory through a versioned Markdown vault, with one `AGENTS.md` as the source of truth

**Planned MVP flow**: clap detection → startup audio → greeting → voice command → spoken response, followed by Telegram notifications and Gmail.

---

### 🤖 DevAssist: CLI AI Agent for Developers
**Agentic AI** | *Personal Project*

A CLI agent built with Pydantic AI that combines GitHub search, web scraping, local file reading and developer utilities.

**Tech Stack**: Pydantic AI, FastMCP, Firecrawl MCP, httpx, Rich, OpenAI, Python 3.12+

**Highlights**:
- Dual MCP integration: a custom FastMCP server plus Firecrawl for full-page scraping, both managed automatically as stdio subprocesses
- Async tool calling with dependency injection through `RunContext`
- Rich CLI with conversation memory and streaming responses

---

### 🔎 Galileu: Production RAG System
**RAG / LLM Engineering** | *Personal Project*

A deployed RAG chatbot with hybrid retrieval, measured with standard information retrieval metrics.

**Tech Stack**: LangChain, ChromaDB, BM25, Llama 3.2, FastAPI, Python, Hugging Face Spaces, Vercel

**Results**:
- **MRR = 1.0, NDCG@8 ≈ 0.91**
- Hybrid BM25 + dense retrieval over 349 indexed chunks
- REST API deployed on Hugging Face Spaces, with the front end on Vercel

---

### 🧠 Finance Phi-3: QLoRA Fine-Tuning
**LLM Fine-Tuning** | *Personal Project*

QLoRA fine-tune of Microsoft's Phi-3-mini-4k-instruct on financial Q&A data.

**Tech Stack**: PyTorch, Hugging Face PEFT, QLoRA, Weights & Biases, Gradio

**Results**:
- **ROUGE-L: 0.218 → 0.499 (+129%)**
- Experiments and training logs tracked in Weights & Biases
- Gradio demo deployed on Hugging Face Spaces

---

### 🏥 Asthma Severity Classifier
**Machine Learning** | *Academic Project*

Asthma severity classification using fuzzy logic.

**Tech Stack**: Python, Fuzzy Logic, scikit-learn

---

## 💻 Tech Stack

### LLMs & Agents
![Pydantic AI](https://img.shields.io/badge/Pydantic_AI-E92063?style=for-the-badge&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=for-the-badge&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=for-the-badge&logo=elevenlabs&logoColor=white)

### Machine Learning & Data
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

### MLOps & Observability
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![Langfuse](https://img.shields.io/badge/Langfuse-0A60B5?style=for-the-badge&logoColor=white)
![Weights & Biases](https://img.shields.io/badge/Weights_%26_Biases-FFBE00?style=for-the-badge&logo=weightsandbiases&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

### Backend & Data Stores
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F00?style=for-the-badge&logoColor=white)

### Cloud
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

---

## 🎓 Education & Certifications

- **B.Sc. in Informatics Engineering**, ISPGAYA *(2025 – 2028, in progress)*
- **42 Porto**, systems programming bootcamp *(completed)*
- **CESAE Digital**, Web & Mobile technician diploma
- **AI/ML certifications (170+ hours):** Generative AI and LLMs, RAG Systems Architecture, Multi-Agent Systems, Cloud Deployment for ML Models, LangChain Development

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=matheusIACreator&show_icons=true&theme=tokyonight)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=matheusIACreator&layout=compact&theme=tokyonight)

---

## 📫 Let's Talk

Hiring for AI/ML Engineering, or want to collaborate on an AI project? Reach out:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/matheus-masago/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:matheus.masago@hotmail.com)
