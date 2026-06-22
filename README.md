<p align="center">
  <img src="./assets/<svg width="760" height="500" viewBox="0 0 760 500" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      .mono { font-family: 'JetBrains Mono', 'Courier New', monospace; }
      .sans { font-family: 'Segoe UI', 'Inter', Arial, sans-serif; }
    </style>

    <!-- Orb gradients -->
    <radialGradient id="orbPurple" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#5B4AE8" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#5B4AE8" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="orbBlue" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#1a6cf0" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#1a6cf0" stop-opacity="0"/>
    </radialGradient>
    <radialGradient id="orbDeep" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#0f4abf" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#0f4abf" stop-opacity="0"/>
    </radialGradient>

    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7B6EF6"/>
      <stop offset="100%" stop-color="#4EA8F0"/>
    </linearGradient>

    <linearGradient id="winFill" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#141416"/>
      <stop offset="100%" stop-color="#0c0c0e"/>
    </linearGradient>

    <filter id="blurBig" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="35"/>
    </filter>

    <clipPath id="rootClip">
      <rect x="0" y="0" width="760" height="500" rx="14"/>
    </clipPath>
    <clipPath id="winClip">
      <rect x="40" y="40" width="680" height="420" rx="12"/>
    </clipPath>
  </defs>

  <!-- ROOT BACKGROUND -->
  <g clip-path="url(#rootClip)">
    <rect x="0" y="0" width="760" height="500" fill="#000000"/>

    <!-- Floating orbs -->
    <g filter="url(#blurBig)">
      <circle cx="40" cy="40" r="160" fill="url(#orbPurple)">
        <animateTransform attributeName="transform" type="translate"
          values="0,0; 30,20; 0,0" dur="8s" repeatCount="indefinite" calcMode="spline"
          keySplines="0.45 0 0.55 1; 0.45 0 0.55 1"/>
      </circle>
      <circle cx="700" cy="460" r="135" fill="url(#orbBlue)">
        <animateTransform attributeName="transform" type="translate"
          values="0,0; -20,-30; 0,0" dur="10s" repeatCount="indefinite" calcMode="spline"
          keySplines="0.45 0 0.55 1; 0.45 0 0.55 1"/>
      </circle>
      <circle cx="470" cy="220" r="95" fill="url(#orbDeep)">
        <animateTransform attributeName="transform" type="translate"
          values="0,0; -25,15; 0,0" dur="12s" repeatCount="indefinite" calcMode="spline"
          keySplines="0.45 0 0.55 1; 0.45 0 0.55 1"/>
      </circle>
    </g>

    <!-- MAC WINDOW -->
    <g>
      <!-- slide-up + fade-in entrance for whole window -->
      <animateTransform attributeName="transform" type="translate"
        values="0,32; 0,0" dur="0.7s" fill="freeze" calcMode="spline"
        keySplines="0.22 1 0.36 1"/>
      <g>
        <animate attributeName="opacity" values="0;1" dur="0.7s" fill="freeze"/>

        <rect x="40" y="40" width="680" height="420" rx="12" fill="url(#winFill)" fill-opacity="0.92" stroke="#ffffff" stroke-opacity="0.1" stroke-width="0.5"/>

        <!-- Title bar -->
        <g clip-path="url(#winClip)">
          <rect x="40" y="40" width="680" height="38" fill="#ffffff" fill-opacity="0.04"/>
          <line x1="40" y1="78" x2="720" y2="78" stroke="#ffffff" stroke-opacity="0.08" stroke-width="0.5"/>
          <circle cx="62" cy="59" r="6" fill="#FF5F57"/>
          <circle cx="82" cy="59" r="6" fill="#FEBC2E"/>
          <circle cx="102" cy="59" r="6" fill="#28C840"/>
          <text x="407" y="63" text-anchor="middle" class="mono" font-size="11" fill="#ffffff" fill-opacity="0.3" letter-spacing="0.5">~/abhay — zsh</text>
        </g>

        <!-- Body content -->
        <g class="mac-body">
          <!-- greeting -->
          <text x="72" y="112" class="mono" font-size="11" fill="#ffffff" fill-opacity="0" letter-spacing="1.1">
            // hello.world
            <animate attributeName="fill-opacity" values="0;0.3" begin="0.3s" dur="0.5s" fill="freeze"/>
          </text>

          <!-- name line -->
          <text x="72" y="150" class="sans" font-size="26" font-weight="600" fill="#ffffff" fill-opacity="0">
            I'm <tspan fill="url(#nameGrad)">Abhay Yadav</tspan>
            <animate attributeName="fill-opacity" values="0;1" begin="0.4s" dur="0.5s" fill="freeze"/>
          </text>

          <!-- tagline -->
          <text x="72" y="176" class="sans" font-size="13" fill="#ffffff" fill-opacity="0">
            18 · India · building things that think
            <animate attributeName="fill-opacity" values="0;0.45" begin="0.5s" dur="0.5s" fill="freeze"/>
          </text>

          <!-- typing / phrase loop line -->
          <g>
            <animate attributeName="opacity" values="0;1" begin="0.6s" dur="0.5s" fill="freeze"/>

            <text x="72" y="212" class="mono" font-size="13" fill="#7B6EF6">
              <tspan>AI / Backend Engineer</tspan>
              <animate attributeName="opacity" values="0;1;1;0" keyTimes="0;0.08;0.42;0.5"
                dur="12s" begin="1s" repeatCount="indefinite"/>
            </text>
            <text x="72" y="212" class="mono" font-size="13" fill="#7B6EF6">
              <tspan>Building AI-driven products</tspan>
              <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.5;0.58;0.92;1"
                dur="12s" begin="1s" repeatCount="indefinite"/>
            </text>
            <text x="72" y="212" class="mono" font-size="13" fill="#7B6EF6">
              <tspan>RAG systems &amp; LLM tooling</tspan>
              <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.917;0.96;1.42;1.5"
                dur="24s" begin="1s" repeatCount="indefinite"/>
            </text>
            <text x="72" y="212" class="mono" font-size="13" fill="#7B6EF6">
              <tspan>Open to Founding Engineer roles</tspan>
              <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.79;0.83;0.99;1"
                dur="36s" begin="1s" repeatCount="indefinite"/>
            </text>

            <!-- blinking cursor -->
            <rect x="280" y="200" width="2" height="14" fill="#7B6EF6">
              <animate attributeName="opacity" values="1;1;0;0;1" keyTimes="0;0.45;0.5;0.95;1" dur="1s" repeatCount="indefinite"/>
            </rect>
          </g>

          <!-- divider 1 -->
          <line x1="72" y1="232" x2="688" y2="232" stroke="#ffffff" stroke-opacity="0" stroke-width="0.5">
            <animate attributeName="stroke-opacity" values="0;0.07" begin="0.7s" dur="0.5s" fill="freeze"/>
          </line>

          <!-- stack label -->
          <text x="72" y="254" class="mono" font-size="10" fill="#ffffff" fill-opacity="0.25" letter-spacing="1.2">STACK</text>

          <!-- badges -->
          <g class="mono" font-size="10" font-weight="500" opacity="0">
            <animate attributeName="opacity" values="0;1" begin="0.8s" dur="0.5s" fill="freeze"/>

            <!-- row 1 -->
            <rect x="72" y="265" width="62" height="20" rx="4" fill="#7B6EF6" fill-opacity="0.12" stroke="#7B6EF6" stroke-opacity="0.35" stroke-width="0.5"/>
            <text x="103" y="279" text-anchor="middle" fill="#9B8FFA">FastAPI</text>

            <rect x="142" y="265" width="58" height="20" rx="4" fill="#7B6EF6" fill-opacity="0.12" stroke="#7B6EF6" stroke-opacity="0.35" stroke-width="0.5"/>
            <text x="171" y="279" text-anchor="middle" fill="#9B8FFA">Python</text>

            <rect x="208" y="265" width="98" height="20" rx="4" fill="#7B6EF6" fill-opacity="0.12" stroke="#7B6EF6" stroke-opacity="0.35" stroke-width="0.5"/>
            <text x="257" y="279" text-anchor="middle" fill="#9B8FFA">RAG Pipelines</text>

            <rect x="314" y="265" width="62" height="20" rx="4" fill="#4EA8F0" fill-opacity="0.1" stroke="#4EA8F0" stroke-opacity="0.3" stroke-width="0.5"/>
            <text x="345" y="279" text-anchor="middle" fill="#6DB8F4">Next.js</text>

            <rect x="384" y="265" width="56" height="20" rx="4" fill="#4EA8F0" fill-opacity="0.1" stroke="#4EA8F0" stroke-opacity="0.3" stroke-width="0.5"/>
            <text x="412" y="279" text-anchor="middle" fill="#6DB8F4">React</text>

            <rect x="448" y="265" width="80" height="20" rx="4" fill="#4EA8F0" fill-opacity="0.1" stroke="#4EA8F0" stroke-opacity="0.3" stroke-width="0.5"/>
            <text x="488" y="279" text-anchor="middle" fill="#6DB8F4">TypeScript</text>

            <!-- row 2 -->
            <rect x="72" y="293" width="76" height="20" rx="4" fill="#28C864" fill-opacity="0.08" stroke="#28C864" stroke-opacity="0.25" stroke-width="0.5"/>
            <text x="110" y="307" text-anchor="middle" fill="#5DC98A">Supabase</text>

            <rect x="156" y="293" width="76" height="20" rx="4" fill="#28C864" fill-opacity="0.08" stroke="#28C864" stroke-opacity="0.25" stroke-width="0.5"/>
            <text x="194" y="307" text-anchor="middle" fill="#5DC98A">ChromaDB</text>

            <rect x="240" y="293" width="52" height="20" rx="4" fill="#ffffff" fill-opacity="0.05" stroke="#ffffff" stroke-opacity="0.12" stroke-width="0.5"/>
            <text x="266" y="307" text-anchor="middle" fill="#ffffff" fill-opacity="0.5">Groq</text>

            <rect x="300" y="293" width="80" height="20" rx="4" fill="#ffffff" fill-opacity="0.05" stroke="#ffffff" stroke-opacity="0.12" stroke-width="0.5"/>
            <text x="340" y="307" text-anchor="middle" fill="#ffffff" fill-opacity="0.5">LangGraph</text>

            <rect x="388" y="293" width="84" height="20" rx="4" fill="#ffffff" fill-opacity="0.05" stroke="#ffffff" stroke-opacity="0.12" stroke-width="0.5"/>
            <text x="430" y="307" text-anchor="middle" fill="#ffffff" fill-opacity="0.5">JWT · RBAC</text>
          </g>

          <!-- divider 2 -->
          <line x1="72" y1="332" x2="688" y2="332" stroke="#ffffff" stroke-opacity="0" stroke-width="0.5">
            <animate attributeName="stroke-opacity" values="0;0.07" begin="0.9s" dur="0.5s" fill="freeze"/>
          </line>

          <!-- find me label -->
          <text x="72" y="354" class="mono" font-size="10" fill="#ffffff" fill-opacity="0.25" letter-spacing="1.2">FIND ME</text>

          <!-- contact links -->
          <g class="mono" font-size="11" fill-opacity="0" letter-spacing="0.4">
            <animate attributeName="fill-opacity" values="0;1" begin="1.0s" dur="0.5s" fill="freeze"/>
            <a href="https://github.com/abhaydv77" target="_blank">
              <text x="72" y="374" fill="#ffffff" fill-opacity="0.6">github.com/abhaydv77</text>
              <line x1="72" y1="378" x2="218" y2="378" stroke="#ffffff" stroke-opacity="0.2" stroke-width="0.5"/>
            </a>
            <text x="234" y="374" fill="#ffffff" fill-opacity="0.6">linkedin</text>
            <line x1="234" y1="378" x2="282" y2="378" stroke="#ffffff" stroke-opacity="0.2" stroke-width="0.5"/>
            <text x="298" y="374" fill="#ffffff" fill-opacity="0.6">twitter / x</text>
            <line x1="298" y1="378" x2="358" y2="378" stroke="#ffffff" stroke-opacity="0.2" stroke-width="0.5"/>
          </g>
        </g>
      </g>
    </g>
  </g>
</svg>
<img width="760" height="500" alt="abhay_github_profile_readme" src="https://github.com/user-attachments/assets/5b87092f-e681-443f-a030-a641123c6963" />
" width="100%">
</p>

# Hi, I'm Abhay Yadav 👋

### AI / GenAI Engineer · Self-Taught · Builder

Self-taught AI/backend engineer focused on building agentic AI systems, RAG pipelines, and automation workflows using Python. Currently exploring multi-agent architectures, self-healing retrieval systems, backend infrastructure, and production-oriented AI applications.

I enjoy learning through building, solving difficult problems independently, and experimenting with real-world AI workflows. My current focus is on AI agents, retrieval systems, backend engineering, and production-oriented AI infrastructure.

---

# 🚀 What I'm Working On

* Multi-Agent AI Systems
* Self-Healing RAG Architectures
* LLM Orchestration & Automation
* Backend APIs with FastAPI
* Retrieval Pipelines & Vector Databases
* AI Workflow Reliability & Evaluations
* Production-Oriented AI Systems

---

# 🧠 Tech Stack

## Languages

* Python
* Basic TypeScript

## AI / GenAI

* LangChain
* LangGraph
* RAG Pipelines
* Prompt Engineering
* Agentic Workflows
* OpenAI APIs
* Groq APIs
* Vector Databases (FAISS, ChromaDB)

## Backend

* FastAPI
* REST APIs
* API Integrations
* OAuth Basics

## Tools & Workflow

* Git & GitHub
* Airtable API
* Debugging & Iteration
* AI-Assisted Development

## Currently Learning

* Docker
* Deployment & Cloud Basics
* Observability
* System Design
* AI Evaluations
* Production Reliability

---

# 📌 Featured Projects
---


## 🔹 Court-AI — Intelligent Court Document Digitization Pipeline
Built an end-to-end AI-powered pipeline that transforms raw scanned court documents (PDF/JPG/PNG) into searchable, structured digital records — reducing manual data entry workforce by 80%.

### Key Features
* OCR pipeline with EasyOCR + Google Cloud Vision fallback
* Hybrid metadata extraction — Regex + Groq LLM (Llama 3.3 70B)
* Automatic QC scoring — approved / review / rescan flagging
* Unique barcode generation (CRT-YYYY-XXXXXXXX) per document
* Searchable PDF generation with embedded OCR text layer
* PostgreSQL — full audit trail, case grouping, duplicate detection
* Excel + CSV report export
* Next.js + Tailwind dark-themed dashboard with live pipeline status

### Focus Areas
* Production-level AI automation
* Hindi + English document processing
* Real-world government digitization workflows
* Full-stack architecture (Python + TypeScript)

🔗 Repository: <https://github.com/abhaydv77/courtAItool>

---

## 🔹 Self-Healing RAG System with Chatbot

Built a self-healing Retrieval-Augmented Generation (RAG) system capable of detecting incorrect or low-quality information in source documents and autonomously generating corrected responses using LLM-based reasoning workflows.

### Key Features

* Document ingestion & chunking pipelines
* Embedding-based retrieval workflows
* Automated issue detection & correction logic
* Structured patch/update generation
* Chatbot interaction APIs
* Logging & workflow tracking systems

### Focus Areas

* Retrieval reliability
* Hallucination reduction
* Agentic reasoning workflows
* Production-oriented backend architecture

🔗 Repository: <https://github.com/abhaydv77/SELF-HEALING-RAG>

---

## 🔹 Multi-Agent Email Automation System

Designed and built a multi-agent workflow using LangGraph that automatically classifies incoming emails into categories such as CVs, Complaints, and Ideas using LLM-powered routing.

### Key Features

* Multi-agent routing using LangGraph StateGraph
* Conditional workflow execution
* Gmail API integration with OAuth 2.0
* Airtable integration for structured data storage
* Automated scheduler for background processing
* Robust JSON parsing for inconsistent LLM outputs

### Focus Areas

* Workflow orchestration
* Automation pipelines
* API integrations
* Reliable AI processing

🔗 Repository: <https://github.com/abhaydv77/multi-agent-email-system>

---

 ## 🚧 Currently Building: HR Policy RAG Bot
🔗 Repository: https://github.com/abhaydv77/HR-RAG

I'm building an HR Policy RAG (Retrieval-Augmented Generation) chatbot to learn how modern AI applications are built beyond simple API wrappers.

### Why I'm Building This

Most AI projects stop at sending prompts to an LLM. I wanted to understand how production AI systems combine:

* Authentication and user identity
* Structured relational data
* Vector databases and semantic search
* Retrieval-Augmented Generation (RAG)
* Backend APIs and application architecture

### What I'm Learning

Through this project I'm learning:

* FastAPI backend development
* JWT authentication and authorization
* SQLAlchemy and relational database design
* Vector databases (ChromaDB)
* Embeddings and semantic search
* RAG pipeline design
* Prompt engineering and context management
* Production-style project structure
* AI-assisted development workflows using CLI tools like OpenCode

### How AI Is Used

The chatbot doesn't rely only on an LLM.

For every question:

1. Relevant HR policy sections are retrieved from a vector database.
2. Employee-specific information is fetched from a relational database.
3. Both sources are combined into a single context.
4. The LLM generates an answer grounded in company policies and employee data.

This helps reduce hallucinations while providing personalized responses.

### Development Workflow

I build most of the backend myself while using AI tools to accelerate learning and development.

* Using OpenCode as a CLI AI assistant for backend development
* Learning by reviewing, modifying, and understanding generated code
* Using AI to explore new concepts, debug issues, and improve implementation details
* Focusing on understanding the architecture rather than blindly copying code

### Current Status

✅ Authentication system

✅ Employee database

✅ Document chunking and embeddings

✅ ChromaDB vector search

✅ End-to-end RAG pipeline

✅ FastAPI API endpoints

🔄 Improving retrieval quality and expanding policy coverage

### Next Steps

🚧 Create a Dockerfile and containerize the application

🚧 Connect the project to Supabase for managed database services

🚧 Build a frontend using React with AI-assisted development

🚧 Integrate frontend and backend into a complete application

🚧 Deploy the project and learn the end-to-end production workflow

### Goal

The goal is not just to build a chatbot, but to understand how real-world AI systems are designed, secured, deployed, and maintained. By the end of this project, I want to gain hands-on experience with backend development, vector databases, cloud services, containerization, frontend development, deployment, and effective use of AI-assisted engineering tools.


# 🎯 What Drives Me

I’m deeply interested in understanding how modern AI systems work under the hood — not just building demos, but designing systems that are reliable, scalable, and useful in real-world environments.

I like working on difficult problems, learning fast, and building projects that push me beyond my current level.

---

# 📫 Connect With Me

* GitHub: [https://github.com/abhaydv77](https://github.com/abhaydv77)
* LinkedIn: [https://www.linkedin.com/in/abhaydv77/](https://www.linkedin.com/in/abhaydv77/)
* Email: [ydvabhay99@gmail.com](mailto:ydvabhay99@gmail.com)

---

# ⚡ Fun Fact

Most of my learning comes from building real projects, getting stuck, debugging for hours, and figuring things out one problem at a time.



# resume 
----------------
[Resume.pdf] [Abhay_Yadav_Resume_v3.pdf](https://github.com/user-attachments/files/29107425/Abhay_Yadav_Resume_v3.pdf)


