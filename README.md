<div align="center">

# Ponsubash Raj R

### Software Engineer focused on Agentic AI, System Design, and Cloud-Native AI Applications

I build AI systems that are useful beyond the demo: agentic workflows, retrieval systems, durable background jobs, and cloud architectures that can survive real constraints.

[![GitHub](https://img.shields.io/badge/GitHub-JustATalentedGuy-181717?style=for-the-badge&logo=github)](https://github.com/JustATalentedGuy)
[![Website](https://img.shields.io/badge/Website-Ponsubash%20Raj-3B82F6?style=for-the-badge&logo=googlechrome&logoColor=white)](https://justatalentedguy.github.io/Ponsubash-Raj/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ponsubash%20Raj-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ponsubashraj/)
[![Email](https://img.shields.io/badge/Email-justatalentedguy%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:justatalentedguy@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-JustACoolGuy-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/JustACoolGuy/)
[![ORCiD](https://img.shields.io/badge/ORCiD-0009--0000--7761--4826-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0009-0000-7761-4826)

</div>

---

## About Me

I am a Software Engineer with a strong interest in building production-grade AI systems. My work sits at the intersection of agentic AI, backend architecture, retrieval systems, and cloud deployment.

I care deeply about the engineering details that make intelligent systems reliable: queues, retries, rate limits, durable state, user isolation, observability, vector retrieval quality, and clean boundaries between AI orchestration and product infrastructure.

Currently, I am focused on:

- Agentic AI workflows and tool-using systems
- RAG systems with hybrid retrieval and grounded generation
- MCP integrations for useful AI interfaces
- Cloud-native AI backends using AWS, Docker, Redis, PostgreSQL, and object storage
- System design patterns for durable, async, multi-stage AI pipelines

---

## Technical Focus

<table>
  <tr>
    <td><strong>Agentic AI</strong></td>
    <td>RAG, tool calling, LangGraph, MCP, structured LLM outputs, grounded Q&A, feedback loops</td>
  </tr>
  <tr>
    <td><strong>Backend Systems</strong></td>
    <td>FastAPI, async workers, Celery, Redis, PostgreSQL, pgvector, Qdrant, API design</td>
  </tr>
  <tr>
    <td><strong>Cloud Architecture</strong></td>
    <td>AWS EC2, S3, IAM, CloudWatch, Docker, Nginx, GitHub Actions, Render, Supabase</td>
  </tr>
  <tr>
    <td><strong>AI Engineering</strong></td>
    <td>Groq, Anthropic, sentence-transformers, Whisper, OCR, evaluation, embeddings, retrieval</td>
  </tr>
  <tr>
    <td><strong>Frontend/Product</strong></td>
    <td>React, TypeScript, Vite, Tailwind CSS, Expo, React Native, VS Code Extension API</td>
  </tr>
</table>

---

## Featured Projects

### CourseFlow

Self-hosted AI learning platform that turns YouTube playlists into structured, searchable, reviewable courses.

**What it does:** Ingests playlists, extracts transcripts, generates durable notes, creates quizzes and spaced-repetition cards, supports semantic search, exports courses, enriches diagrams, and exposes a local MCP server for Claude Desktop.

**System design highlights:**

- Durable Celery workflows with Redis-backed queues
- PostgreSQL + pgvector as the core source of truth and retrieval layer
- Groq quota-aware scheduling with retry and backpressure handling
- Local edge fetcher for YouTube calls sensitive to cloud-IP blocking
- MinIO/S3 object storage for generated artifacts
- AWS deployment with EC2, IAM, CloudWatch, Docker, and GitHub Actions OIDC

**Stack:** FastAPI, PostgreSQL, pgvector, Redis, Celery, MinIO/S3, Groq, LangGraph, Cloudflare Workers AI, Docker, AWS, MCP

[Repository](https://github.com/JustATalentedGuy/courseflow)

---

### Docflow

Multi-user document question-answering system for PDFs and images.

**What it does:** Lets users upload documents, process them asynchronously, extract text/OCR, chunk content, search with hybrid retrieval, and ask grounded questions in user-isolated chats.

**System design highlights:**

- User-scoped files, chats, messages, S3 keys, and vector payloads
- Celery + Redis document processing pipeline
- Parent-child chunking for retrieval precision and answer context
- Qdrant vector search plus BM25 keyword search
- Reciprocal Rank Fusion for hybrid retrieval
- AWS demo deployment with EC2, S3, PostgreSQL, Redis, Qdrant, Nginx, and CloudWatch

**Stack:** FastAPI, React, Celery, Redis, PostgreSQL, Qdrant, MinIO/S3, Tesseract OCR, PyMuPDF, LangGraph, Groq, Docker, AWS

[Repository](https://github.com/JustATalentedGuy/docflow)

---

### Pulse

Personal AI intelligence reader for engineers and researchers.

**What it does:** Collects content from RSS, GitHub, arXiv, and Gmail newsletters, enriches it with LLMs, ranks it based on behavior, and serves a personalized mobile feed with search, quizzes, digests, trends, and grounded Q&A.

**System design highlights:**

- Multi-source ingestion with normalization, deduplication, and failure isolation
- PostgreSQL + pgvector for semantic and hybrid search
- Groq enrichment for summaries, categories, entities, and scoring
- LangGraph Socratic quizzes and corpus-grounded Ask mode
- Expo mobile app with offline cache and network-aware states
- Local Docker path and free-tier Render + Supabase deployment path

**Stack:** FastAPI, PostgreSQL, pgvector, Groq, LangGraph, Expo, React Native, Supabase, Render, Docker, GitHub Actions

[Repository](https://github.com/JustATalentedGuy/pulse)

---

### Smart Notes Generator

Local-first study notes app that turns lecture PDFs and slides into structured notes while preserving diagrams in context.

**What it does:** Extracts text and figures, filters diagrams, builds placeholder-aware prompts, generates notes, restores original images, evaluates quality locally, supports RAG Q&A, and exports notes.

**System design highlights:**

- Local-first privacy boundary where source files and images stay on the machine
- Placeholder-based diagram preservation to avoid expensive image-token usage
- SQLite-backed saved notes library
- Local faithfulness and coverage evaluation
- Semantic retrieval with TF-IDF/Jaccard fallbacks
- Agent refinement for scoped edits while preserving figures

**Stack:** FastAPI, React, TypeScript, Anthropic, SQLite, PyMuPDF, python-pptx, Pillow, sentence-transformers, scikit-learn, WeasyPrint

[Repository](https://github.com/JustATalentedGuy/SmartNotes)

---

## Toolbox

### Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)

### AI and Data

![LangGraph](https://img.shields.io/badge/LangGraph-111111?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![sentence-transformers](https://img.shields.io/badge/sentence--transformers-0B5FFF?style=flat-square)

### Backend and Infra

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)

### Frontend and Product

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)
![VS Code API](https://img.shields.io/badge/VS_Code_Extension_API-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)

---

## Engineering Principles I Like

- Prefer durable workflows over fragile one-shot scripts.
- Keep AI systems grounded with retrieval, schemas, evaluation, and source boundaries.
- Separate transient state from persistent state.
- Design for failure: retries, rate limits, backpressure, observability, and clear recovery paths.
- Treat cloud architecture as part of product design, not an afterthought.
- Build tools that help users think better, not just move faster.

---

## GitHub Snapshot

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=JustATalentedGuy&show_icons=true&theme=github_dark&hide_border=true&rank_icon=github" alt="GitHub stats" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=JustATalentedGuy&layout=compact&theme=github_dark&hide_border=true" alt="Top languages" />

<br />

<img src="https://streak-stats.demolab.com?user=JustATalentedGuy&theme=github-dark-blue&hide_border=true" alt="GitHub streak" />

</div>

---

## Current Direction

I am especially interested in roles and collaborations around:

- AI engineering
- Agentic systems
- RAG and retrieval infrastructure
- Backend/platform engineering
- Cloud architecture for AI products
- Developer tools and learning systems

If you are building systems where AI has to interact with real users, real data, real latency, and real failure modes, I would love to connect.

<div align="center">

### Let's Build Useful AI Systems

[Website](https://justatalentedguy.github.io/Ponsubash-Raj/) | [LinkedIn](https://www.linkedin.com/in/ponsubashraj/) | [GitHub](https://github.com/JustATalentedGuy) | [Email](mailto:ponsubashraj2370043@ssn.edu.in) | [LeetCode](https://leetcode.com/u/JustACoolGuy/) | [ORCiD](https://orcid.org/0009-0000-7761-4826)

</div>
