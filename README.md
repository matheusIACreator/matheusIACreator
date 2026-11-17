# 👋 Hi, I'm Matheus

**AI/ML Engineer based in Porto, Portugal.** I build LLM applications and ML systems, and I own what happens after the demo: evaluation, security, observability, CI/CD and compliance.

Today I run a multilingual GenAI chatbot in production at Living Tours, from architecture to deployment. My full-stack background (Next.js, React, TypeScript) means I can take a model all the way to a product people actually use.

**What I work on:** RAG · Agentic AI · Voice AI · LLM evaluation & guardrails · LLM fine-tuning · MLOps

📍 **Open to AI/ML Engineer roles:** hybrid in Porto or remote.

---

## 🌟 Professional Experience

### AI & Web Developer @ Living Tours
*Porto, Portugal · May 2026 – Present*

I own the full lifecycle of the Living Cruise GenAI chatbot, running in production in four languages (PT/EN/ES/FR).

- **Architecture:** led the migration from AWS Lambda + Groq to Cloudflare Workers, Containers and Workers AI, with a FastAPI (Python 3.13) and PostgreSQL backend, shipped with Docker and Wrangler
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

Four projects that bring together my work in ML systems, voice agents, cloud delivery and retrieval.

### 🏨 hotelml: End-to-End MLOps Platform

**MLOps · Predictive ML** | *Personal project · In active development*

[**Live demo**](https://hotelml.vercel.app) · [**Repository**](https://github.com/matheusIACreator/Hotel-Demand)

A platform for hotel booking cancellation prediction that covers reproducible training, model management, serving and operational tooling.

**Stack:** Python, scikit-learn, MLflow, FastAPI, Docker, Terraform, Azure Container Apps, GitHub Actions, PySpark, Next.js

- **Evaluation:** ROC-AUC **0.8614**, PR-AUC **0.8234** and F1 **0.6936** on a temporal test set of **23,842 bookings**, from 119,390 raw rows. These are offline evaluation results, not production traffic metrics.
- **Model lifecycle:** MLflow tracking, champion/challenger registry, conditional promotion, exported model bundles and rollback.
- **Deployment:** containerized FastAPI on Azure Container Apps, Terraform infrastructure and GitHub Actions CD with OIDC, images pinned by digest and post-deploy smoke tests.
- **Data pipelines:** PySpark feature engineering and batch scoring validated locally, with parity checks against the scikit-learn pipeline.
- **Operations:** structured telemetry, configurable Azure alerts, drift and model-quality tooling, plus architecture decisions and runbooks.

**Current scope:** API and frontend published; Spark pipelines validated locally. Monitoring and retraining tools are implemented, while operational rollout still depends on approved targets, pilot completion and a real source of booking outcomes. LLMOps remains planned.

---

### 🎙️ Jarvis: Personal Voice Assistant

**Voice AI · Agentic AI** | *Personal project · Working MVP*

[**Repository**](https://github.com/matheusIACreator/jarvis-ai)

A Windows voice assistant that combines local speech recognition, Claude tool calling and streaming speech synthesis, with Telegram and a local web dashboard.

**Stack:** Python, Anthropic API, faster-whisper, ElevenLabs, Telegram Bot API, Next.js, React

**Flow:** double clap or wake word → local transcription → Claude with tools → streaming voice reply

- **Conversation:** persistent voice sessions with Claude Haiku by default and Sonnet on demand.
- **Confirmed actions:** outgoing Telegram messages require explicit confirmation, which expires after 60 seconds.
- **Background reasoning:** longer tasks run while the conversation continues and deliver their results through Telegram.
- **Searchable memory:** voice, Telegram and web exchanges are saved locally as Obsidian-compatible Markdown and retrieved without embeddings or a cloud memory service.
- **Dashboard:** local Next.js interface with assistant status and text chat.

**Current scope:** a single-user local assistant. Background tasks have no web, file or command access; email and phone calls remain planned.

---

### ☁️ DevOps Lab: Azure Mission Control

**DevOps · Cloud Infrastructure · CI/CD** | *Personal project*

[**Live demo**](https://ca-devops-lab.mangoplant-1a4839a2.northeurope.azurecontainerapps.io) · [**Repository**](https://github.com/matheusIACreator/devops-lab)

An end-to-end Azure lab that connects a Next.js application and instrumented APIs to reproducible infrastructure and deployment workflows.

**Stack:** Next.js, React, TypeScript, Docker, Terraform, GitHub Actions, Azure Container Apps, Azure Container Registry, Log Analytics, Playwright

- **Infrastructure:** Terraform-managed Azure resources, managed identities and scale-to-zero container hosting.
- **CI/CD:** lint, type checks, application and Docker builds, container smoke tests and Terraform validation; manual deployments authenticate through OIDC.
- **Deployment verification:** smoke tests wait for the expected application revision, followed by desktop and mobile Playwright checks.
- **Observability:** request IDs, server timing and structured JSON logs, with a dashboard showing real API measurements from the browser session.
- **Operational practice:** load-testing scripts, image-based manual rollback and documented cost and teardown procedures.

**Measurement scope:** dashboard metrics describe the current browser session; they are not Azure-wide monitoring aggregates.

---

### 🔎 Galileu: Hybrid RAG for Historical Q&A

**RAG · LLM Engineering** | *Personal project*

[**Live demo**](https://langchain-project-nine.vercel.app/) · [**Repository**](https://github.com/matheusIACreator/Langchain_Project)

A deployed historical Q&A application covering Galileo, Newton and Einstein, with hybrid retrieval, multilingual embeddings and conversational context.

**Stack:** Python, LangChain, ChromaDB, BM25, Llama 3.2 3B, FastAPI, Next.js, Hugging Face Spaces, Vercel

- **Retrieval:** BM25 and dense semantic search combined through Reciprocal Rank Fusion over **349 indexed chunks**.
- **Evaluation:** **MRR = 1.0** and **NDCG@8 ≈ 0.91** on the project's manually labeled retrieval evaluation set.
- **Interaction:** topic routing across three knowledge bases and multi-turn conversation memory.
- **Delivery:** Dockerized FastAPI backend on Hugging Face Spaces and a Next.js frontend on Vercel.
- **Testing:** coverage of routing, conversation memory, hybrid retrieval and the end-to-end pipeline.

**Evaluation scope:** retrieval metrics describe the labeled query set; they do not measure factual accuracy across all generated answers.

---

## 🧪 More Projects

- [**DevAssist**](https://github.com/matheusIACreator/DevAssist) — CLI developer agent with Pydantic AI, asynchronous tool calling, structured outputs and custom + Firecrawl MCP integrations.
- [**Finance Phi-3 QLoRA**](https://github.com/matheusIACreator/finance-phi3-qlora) — financial Q&A fine-tuning: ROUGE-L **0.218 → 0.499** on the project evaluation, training **0.23%** of parameters.
- [**Churn Risk Detector**](https://github.com/matheusIACreator/Churn-evaluator) — XGBoost classification with SHAP explanations and a Streamlit interface; reported ROC-AUC **0.8446** and churn recall **82%**.
- [**JAX RALM**](https://github.com/matheusIACreator/jax-ralm) — experimental retrieval-augmented transformer built with JAX/Flax, FAISS and cross-attention, with a small-scale ablation study.
- [**Expense Classifier**](https://github.com/matheusIACreator/Expenses-Classifier) — TF-IDF and logistic regression served through FastAPI; weighted F1 **0.83** on synthetic transaction descriptions.
- [**Asthma Severity Classifier**](https://github.com/matheusIACreator/AsthmaModel) — academic fuzzy-logic application built with Python, scikit-fuzzy and Streamlit.

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
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
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

## 📫 Let's Talk

Hiring for AI/ML Engineering, or want to collaborate on an AI project? Reach out:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/matheus-masago/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:matheus.masago@hotmail.com)
