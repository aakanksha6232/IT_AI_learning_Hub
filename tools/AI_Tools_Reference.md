# 🛠 AI Tools Reference — Curated for Enterprise IT Teams

> A practical, role-tagged reference of AI tools your team will encounter in the roadmap.  
> Tags: `[BA]` Business Analyst · `[QA]` Tester · `[DEV]` Developer · `[ALL]` Everyone

---

## 🤖 LLM Frameworks & Orchestration

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **LangChain** | Build chains, agents, memory, and tool-use workflows | `[DEV]` | Go-to for most Python AI pipelines. Extensive ecosystem. |
| **LlamaIndex** | Connect LLMs to structured and unstructured data | `[DEV]` | Strong for document ingestion, data connectors, and query pipelines |
| **LangGraph** | Build stateful multi-agent systems with conditional loops | `[DEV]` `[QA]` | Extends LangChain; built for complex agent state machines |
| **AutoGen** | Multi-agent conversation frameworks | `[DEV]` | Microsoft-backed; good for agent collaboration patterns |
| **CrewAI** | Role-based multi-agent orchestration | `[DEV]` | Simpler API than LangGraph for role-assigned agent teams |

---

## 🔍 RAG & Vector Databases

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **Pinecone** | Managed vector database | `[DEV]` | Fully managed; fastest time-to-production for RAG |
| **Weaviate** | Open-source vector DB with GraphQL API | `[DEV]` | Strong hybrid search (vector + keyword) |
| **pgvector** | Vector search extension for PostgreSQL | `[DEV]` | Best option if your team already runs PostgreSQL |
| **Chroma** | Open-source, local-first vector DB | `[DEV]` | Ideal for prototyping and local development |
| **Qdrant** | High-performance vector DB written in Rust | `[DEV]` | Good for production deployments requiring low latency |
| **FAISS** | Facebook AI Similarity Search library | `[DEV]` | Open-source; excellent for offline/on-premises RAG |

---

## 📏 Evaluation & Testing

| Tool | What it measures | Who uses it | Notes |
|------|-----------------|-------------|-------|
| **RAGAS** | Faithfulness · Answer relevance · Retrieval precision | `[DEV]` `[QA]` | Standard framework for RAG quality evaluation |
| **DeepEval** | Hallucination detection · LLM regression testing | `[DEV]` `[QA]` | Integrates with CI/CD; pytest-compatible |
| **LangSmith** | LLM tracing, debugging, and evaluation | `[DEV]` | Built by LangChain team; best-in-class observability |
| **PromptFoo** | Prompt testing and A/B comparison | `[DEV]` | CLI tool; excellent for prompt regression suites |
| **TruLens** | LLM application evaluation | `[DEV]` `[QA]` | Feedback functions for hallucination, relevance, groundedness |

---

## 🔌 MCP Tools & Integrations

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **MCP (Model Context Protocol)** | Open standard for AI ↔ tool integration | `[DEV]` `[BA]` | Anthropic-created; now industry standard |
| **Claude Desktop MCP** | Connect Claude to local tools and APIs | `[DEV]` `[ALL]` | Filesystem, databases, APIs via MCP config |
| **GitHub MCP Server** | AI access to GitHub repos and issues | `[DEV]` | Official GitHub MCP server |
| **Zapier MCP** | Connect AI agents to 5000+ SaaS apps | `[DEV]` `[BA]` | No-code MCP bridge to enterprise tools |

---

## 🛡 Safety & Guardrails

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **openai-guardrails-python** | Configurable safety and compliance layer | `[DEV]` `[QA]` | Input/output moderation; policy enforcement |
| **NeMo Guardrails** | NVIDIA's programmable guardrails for LLMs | `[DEV]` | Rails defined in YAML; good for enterprise compliance |
| **LlamaGuard** | Meta's content safety model for LLM I/O | `[DEV]` | Open-source safety classifier; integrate as a filter |
| **Presidio** | Microsoft's PII detection and anonymisation | `[DEV]` | Redact sensitive data from LLM inputs and outputs |

---

## 🖥 Local LLM Runtime

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **Ollama** | Run LLMs locally — simple CLI | `[DEV]` `[ALL]` | Easiest way to run Llama, Mistral, Qwen locally |
| **LM Studio** | GUI for running local LLMs | `[DEV]` `[ALL]` | Great for exploration; no coding required |
| **llama.cpp** | C++ inference engine for LLMs | `[DEV]` | Most efficient CPU inference; basis for Ollama |
| **vLLM** | High-throughput LLM serving | `[DEV]` | Production-grade; GPU-optimised serving |
| **Hugging Face Transformers** | Python library for all open-source models | `[DEV]` | De facto standard for model loading and fine-tuning |

---

## 🔬 Embedding Models

| Model | Provider | Context | Notes |
|-------|----------|---------|-------|
| **text-embedding-3-small** | OpenAI | 8K tokens | Cost-efficient; most common default |
| **text-embedding-3-large** | OpenAI | 8K tokens | Higher accuracy; use when retrieval quality matters |
| **nomic-embed-text** | Nomic / Ollama | 8K tokens | Best open-source local embedding model |
| **all-MiniLM-L6-v2** | Hugging Face | 512 tokens | Lightweight; fast; good for CPU inference |
| **BGE (BAAI)** | Hugging Face | 512 tokens | Strong performance on retrieval benchmarks |

---

## 🧪 AI-Assisted Testing Tools

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **GitHub Copilot** | AI pair programmer — test generation | `[DEV]` `[QA]` | Generate test cases from function signatures |
| **Cursor** | AI-native IDE | `[DEV]` | Codebase-aware AI assistant; strong for refactoring |
| **Tabnine** | On-premise AI code completion | `[DEV]` | Privacy-first; self-hostable; good for enterprise |
| **Selenium + AI** | AI-enhanced browser testing | `[QA]` | AI selectors reduce test brittleness |
| **Playwright + Copilot** | AI-generated E2E test scripts | `[QA]` | Copilot writes Playwright tests from natural language |

---

## 📊 LLMOps & Monitoring

| Tool | What it does | Who uses it | Notes |
|------|-------------|-------------|-------|
| **LangSmith** | Tracing, evaluation, and monitoring | `[DEV]` | End-to-end observability for LangChain apps |
| **Weights & Biases** | Experiment tracking and model monitoring | `[DEV]` | LLM prompt + output logging; eval dashboards |
| **MLflow** | MLOps lifecycle management | `[DEV]` | Log prompts, models, evals; multi-framework support |
| **Helicone** | LLM observability and cost tracking | `[DEV]` | Proxy-based; plug in without changing code |
| **Phoenix (Arize)** | Open-source LLM observability | `[DEV]` | Tracing + RAGAS-compatible evaluation |

---

## 🎓 Learning Platforms

| Platform | What it offers | Who it suits | Cost |
|----------|---------------|-------------|------|
| **DeepLearning.AI** | Short courses by Andrew Ng | `[ALL]` | Free short courses; paid specialisations |
| **Hugging Face Learn** | NLP and open-source AI courses | `[DEV]` | Free |
| **Fast.ai** | Practical deep learning from scratch | `[DEV]` | Free |
| **Google ML Crash Course** | Supervised learning foundations | `[DEV]` | Free |
| **Microsoft Learn — AI** | Azure AI and LLMOps paths | `[DEV]` `[LEADER]` | Free |
| **Coursera — AI for Everyone** | Non-technical AI literacy | `[BA]` `[LEADER]` | Free to audit |

---

## 🔗 Quick Setup: Recommended Local Stack

For developers wanting to experiment locally without cloud costs:

```bash
# 1. Install Ollama (local LLM runtime)
curl -fsSL https://ollama.ai/install.sh | sh

# 2. Pull a model
ollama pull llama3.2
ollama pull nomic-embed-text     # for RAG embeddings

# 3. Install Python AI stack
pip install langchain langchain-community chromadb ragas deepeval

# 4. Run a quick RAG test
python -c "from langchain_community.llms import Ollama; print(Ollama(model='llama3.2').invoke('Explain RAG in one sentence'))"
```

---

*Part of the AI Learning Roadmap — [IT AI Learning Hub](https://github.com/aakanksha6232/IT_AI_learning_Hub)*
