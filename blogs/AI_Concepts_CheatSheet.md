# 💡 AI Concepts Cheat Sheet — Plain English for Every Role

> **Who is this for?** Every team member — BA, Tester, Developer, Leader.  
> No prior AI knowledge required. If a concept has a jargon name, this sheet translates it.

---

## The Core Trio: RAG · MCP · Agent

These three concepts appear in almost every enterprise AI conversation in 2026. Understand these first.

---

### 🔍 RAG — Retrieval-Augmented Generation

| | |
|---|---|
| **Role in a System** | Knowledge Layer (Memory) |
| **Core Idea** | Gives the LLM access to your documents, policies, or databases at query time |
| **Human Analogy** | 📚 A researcher who looks up the right book *before* answering your question |
| **What it does** | Fetches relevant chunks from your documents, feeds them as context to the LLM |

**Example Use Cases:**
- "Summarise our insurance policy docs"
- "Answer from our Q3 report"
- "Find relevant clauses in this BRD"

**Why it matters:** LLMs are trained on public data up to a cutoff date. RAG lets them answer questions about *your* private, real-time documents without retraining the model. This is how most enterprise AI Q&A systems work.

---

### 🔌 MCP — Model Context Protocol

| | |
|---|---|
| **Role in a System** | Action Layer (Hands) |
| **Core Idea** | A standard interface that lets an AI agent call APIs, tools, and external systems |
| **Human Analogy** | 🔧 A USB port — plug in any tool and the AI can use it |
| **What it does** | Executes real-world actions: update CRM, send email, query DB, call REST API |

**Example Use Cases:**
- "Update ticket status in Jira"
- "Send summary email to the team"
- "Pull live data from SQL and generate a report"

**Why it matters:** RAG gives AI *knowledge*. MCP gives AI *hands*. Without MCP, AI can only produce text. With MCP, it can take actions in the real world. MCP is an open standard created by Anthropic, now adopted across the industry.

---

### 🤖 AI Agent

| | |
|---|---|
| **Role in a System** | Orchestrator (Brain) |
| **Core Idea** | A system that can plan, decide what to do, use RAG or MCP, and take multi-step actions |
| **Human Analogy** | 🧠 A project manager who decides what to look up (RAG) and what to action (MCP) |
| **What it does** | Plans, reasons, loops, calls tools, handles errors, produces outcomes |

**Example Use Cases:**
- "Review this BRD, find gaps, create Jira tickets, and notify the team" — all autonomously
- "Monitor the inbox, summarise overnight alerts, and update the dashboard by 9am"

**Why it matters:** A Copilot assists you. An Agent acts independently. Knowing the difference is critical for requirements, governance, and architecture decisions.

---

## Supporting Concepts

### 🗂 Embeddings

| | |
|---|---|
| **Role in a System** | Semantic Search Foundation |
| **Core Idea** | Converts text into numbers that capture *meaning* — similar text = similar numbers |
| **Human Analogy** | 📍 A map where similar cities are placed near each other |
| **What it does** | Enables vector search: find documents/chunks by meaning, not just keyword |

**In practice:** RAG uses embeddings to find the most relevant document chunks for any user query. "Contract termination clause" and "end of agreement conditions" become nearby points in embedding space — even though they share no words.

---

### 🗃 Vector Database

| | |
|---|---|
| **Role in a System** | Storage for Embeddings |
| **Core Idea** | A database optimised for storing and searching embeddings at speed |
| **Human Analogy** | 📦 A smart filing cabinet that finds files by meaning, not by file name |
| **What it does** | Stores embedding vectors, returns nearest-neighbour matches in milliseconds |

**Common tools:** Pinecone, Weaviate, pgvector (PostgreSQL extension), Chroma, Qdrant

---

### 🔄 LLMOps

| | |
|---|---|
| **Role in a System** | Operations Layer (DevOps for AI) |
| **Core Idea** | The practice of deploying, monitoring, evaluating, and maintaining LLM applications |
| **Human Analogy** | 🏭 CI/CD + monitoring for AI — like DevOps, but for models and prompts |
| **What it does** | Tracks cost, latency, output quality drift, model refresh cycles, and rollbacks |

**In practice:** A CI pipeline that runs DeepEval on every deploy. A cost alert if inference spend spikes. A dashboard showing hallucination rates over time.

---

### 🛡 Guardrails

| | |
|---|---|
| **Role in a System** | Safety Layer (Compliance) |
| **Core Idea** | Rules and filters applied to LLM inputs and outputs to prevent harm, bias, or data leaks |
| **Human Analogy** | 🚦 Traffic lights for AI — stops the car from going in the wrong direction |
| **What it does** | Blocks unsafe inputs, redacts PII, filters harmful outputs, enforces policies |

**In practice:** Prevent AI from outputting confidential data. Block prompt injection attacks. Enforce regulatory compliance on AI-generated customer communications.

---

### 🔁 HITL — Human-in-the-Loop

| | |
|---|---|
| **Role in a System** | Human-in-the-Loop (Governance) |
| **Core Idea** | A design pattern where a human must review or approve AI output before it acts |
| **Human Analogy** | ✅ A sign-off gate — the AI drafts, a human approves before it goes live |
| **What it does** | Adds an approval step in workflows where AI decisions have real-world consequences |

**The rule:** AI drafts a customer email → human approves → system sends. **Never auto-send.**

**Where HITL is non-negotiable:** financial decisions, legal documents, customer-facing communications, compliance approvals, medical recommendations.

---

## Copilot vs Agent — What's the Difference?

| | Copilot | Agent |
|---|---|---|
| **Who acts?** | Human (AI assists) | AI (human may review) |
| **Initiative** | Responds to prompts | Plans and acts autonomously |
| **Loop** | Single turn | Multi-step loop |
| **Example** | GitHub Copilot suggests code | Coding agent reviews PR, runs tests, fixes bugs, opens PR |
| **Governance need** | Low | High — HITL required |

---

## RAG vs MCP — When to Use Which

| Scenario | Use | Why |
|----------|-----|-----|
| "Answer from our policy documents" | RAG | Knowledge retrieval — no action needed |
| "Summarise the Q3 report" | RAG | Document intelligence |
| "Create a Jira ticket" | MCP | External system action |
| "Send a summary email" | MCP | Real-world action via API |
| "Find clause in BRD, then create Jira task" | RAG + MCP | Both — retrieve then act |
| "Monitor inbox and update dashboard" | Agent + MCP | Autonomous multi-step workflow |

---

## Evaluation Frameworks — Quick Reference

| Tool | What it measures | Who uses it |
|------|-----------------|-------------|
| **RAGAS** | Faithfulness · Answer relevance · Retrieval precision | Testers, Developers |
| **DeepEval** | Hallucination detection · Regression testing | Testers, Developers |
| **LangSmith** | LLM tracing, debugging, evaluation | Developers |
| **PromptFoo** | Prompt testing and regression | Developers |

---

## The AI Literacy Pub Test

Before claiming you understand a concept, apply the **pub test**: can you explain it to a non-technical colleague over lunch without using jargon?

| Concept | One-sentence pub test explanation |
|---------|----------------------------------|
| RAG | "It lets the AI look things up in your own documents before answering." |
| MCP | "It's the plug that lets AI connect to and control real tools and systems." |
| AI Agent | "It's like an AI employee that can plan tasks and get things done without constant supervision." |
| Embeddings | "It turns words and documents into coordinates on a map of meaning." |
| Vector DB | "A database that finds things by what they mean, not by exact keywords." |
| LLMOps | "DevOps for AI — making sure the AI system keeps working well in production." |
| Guardrails | "Safety filters that stop the AI from saying or doing something it shouldn't." |
| HITL | "A checkpoint where a human reviews what the AI did before it actually happens." |

---

*Part of the AI Learning Roadmap — [IT AI Learning Hub](https://github.com/aakanksha6232/IT_AI_learning_Hub)*
