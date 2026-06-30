<img width="760" height="500" alt="abhay_github_profile_readme (1)" src="https://github.com/user-attachments/assets/5d206074-b3ff-47f7-9453-fbd81d494121" /> <svg width="760" height="500" viewBox="0 0 760 500" xmlns="http://www.w3.org/2000/svg">


  # hey, i'm Abhay 👋

18, self-taught. I build AI systems — agents, RAG pipelines, automation workflows.


## what I'm actually working on right now

- multi-agent architectures using LangGraph
- RAG systems that go beyond the basic "chunk → retrieve → prompt" pattern
- backend APIs with FastAPI
- figuring out how to make AI workflows actually reliable in production (not just demo-ready)

## tech I use

**AI / GenAI**
LangGraph · LangChain · RAG pipelines · Prompt Engineering · Groq · OpenAI APIs · ChromaDB · FAISS · Agentic workflows

**Backend**
FastAPI · REST APIs · JWT auth · OAuth · Supabase · PostgreSQL · Redis · WebSockets

**Frontend / Deploy**
Next.js · React · Vercel · (deploying to a better infra than Render soon — had issues)

**DevOps / Tools**
Git · Docker · CI/CD basics · Kubernetes (learning) · Airtable API · OpenCode (my main AI coding assistant)

**Currently learning**
Kubernetes · observability · system design · AI evaluations · production reliability patterns

## projects

### Court-AI — Court Document Digitization Pipeline
Built an end-to-end pipeline that takes raw scanned court documents (PDF/JPG/PNG) and turns them into searchable, structured digital records. The boring-but-real kind of AI work.

**what's inside:**
- OCR pipeline — EasyOCR with Google Cloud Vision as fallback
- metadata extraction using Regex + Groq LLM (Llama 3.3 70B)
- auto QC scoring: approved / needs review / rescan
- unique barcode generation per document (CRT-YYYY-XXXXXXXX format)
- searchable PDFs with embedded OCR text layer
- PostgreSQL for full audit trail, case grouping, duplicate detection
- Excel + CSV export
- Next.js dark dashboard with live pipeline status

Built this to understand what AI automation actually looks like for government-scale document workflows — Hindi + English both supported.

🔗 [github.com/abhaydv77/courtAItool](https://github.com/abhaydv77/courtAItool)

### HR Policy RAG Bot
A full-stack RAG chatbot for HR policy queries. Not a wrapper around ChatGPT — actually built the whole thing.

The idea: most AI demos stop at "send prompt, get response." I wanted to understand what happens when you combine auth, relational data, vector search, and an LLM into something that doesn't hallucinate your company's leave policy.

**stack:**
- FastAPI backend with JWT auth + RBAC (role-based access — employees only see what they're supposed to)
- Supabase (PostgreSQL) for employee + policy data
- ChromaDB for vector search
- SentenceTransformer embeddings + Groq LLM
- Next.js frontend on Vercel
- Backend deployed (Render had some issues, moving to better infra)

**how it works:**
1. question comes in → relevant HR policy chunks retrieved from ChromaDB
2. employee-specific data pulled from Supabase
3. both combined into context → LLM generates a grounded answer

Reduces hallucinations significantly compared to just prompting an LLM cold.

🔗 [github.com/abhaydv77/HR-RAG](https://github.com/abhaydv77/HR-RAG)

### Multi-Agent Email Automation System
LangGraph-based multi-agent workflow that classifies incoming emails (CVs, complaints, ideas, etc.) and routes them automatically. Built this when I wanted to actually learn LangGraph beyond tutorials.

**what's inside:**
- LangGraph StateGraph with conditional routing
- Gmail API with OAuth 2.0
- Airtable for structured storage
- background scheduler for continuous processing
- robust JSON parsing — LLMs sometimes return markdown inside JSON, had to handle that

Debugged a lot of fun stuff: OAuth scope issues, Airtable field mismatches, LLM output inconsistencies. The kind of stuff you only hit when you're building something real.

🔗 [github.com/abhaydv77/multi-agent-email-system](https://github.com/abhaydv77/multi-agent-email-system)

### Self-Healing RAG System
RAG system that detects when retrieved content is low quality or incorrect and tries to fix it autonomously instead of just returning a bad answer.

**what's inside:**
- document ingestion + chunking pipeline
- embedding-based retrieval
- automated issue detection + correction logic
- LLM-based patch generation
- logging throughout

Main focus: hallucination reduction, retrieval reliability, agentic reasoning in a production-style backend.

🔗 [github.com/abhaydv77/SELF-HEALING-RAG](https://github.com/abhaydv77/SELF-HEALING-RAG)

## what actually drives me

I like building things that don't have obvious answers. The parts where you have to figure out why the LLM is returning markdown inside a JSON field at 2am, or why your retrieval quality drops for certain query types. That stuff.

I'm not trying to build demos. I want to understand how production AI systems are designed, where they break, and how to make them not break.

## find me

- GitHub: [abhaydv77](https://github.com/abhaydv77)
- LinkedIn: [abhaydv77](https://www.linkedin.com/in/abhaydv77/)
- X: [abhaydv2](https://x.com/Abhaydv2)
- Email: ydvabhay99@gmail.com



# resume 
----------------
[Resume.pdf] [Abhay_Yadav_Resume_v3.pdf](https://github.com/user-attachments/files/29107425/Abhay_Yadav_Resume_v3.pdf)


