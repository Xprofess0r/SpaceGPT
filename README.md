# 🚀 SpaceGPT  
### Autonomous Agentic RAG System for Space Research Assistance

**Developed at:** Space Technology Cell, ISRO & IIT Kharagpur  
**Duration:** July 2025 – August 2025  

---

## 📌 Overview

**SpaceGPT** is an **autonomous conversational Space Research Assistant** built using an **Agentic Retrieval-Augmented Generation (RAG)** architecture.  
The system is designed to deliver **accurate, context-aware, and reliable responses** to space science queries by combining:

- Knowledge-base grounded retrieval  
- Tool-assisted reasoning  
- Autonomous, self-correcting agent workflows  

The project emphasizes **evaluation-driven development, observability, and scalability** for real-world research use cases.

---

## 🎯 Key Features

- ✅ Agentic RAG with grounded responses  
- ✅ Autonomous tool calling & web search  
- ✅ Self-correcting agent workflow  
- ✅ Quantitative RAG evaluation (RAGAS)  
- ✅ Full observability with LangSmith  
- ✅ Scalable FastAPI backend  

---

## 🧠 System Architecture (High Level)

User Query
↓
Agent Controller
↓
Knowledge Retrieval (LlamaIndex)
↓ (if insufficient context)
Web Search Tool (LangChain)
↓
Answer Generation (LLM)
↓
Self-Correction & Validation (LangGraph)
↓
Final Response

yaml
Copy code

---

## 🏗️ Project Structure

space_gpt/
├── app/ # FastAPI application & API routes
│ ├── agents/ # LangGraph agent workflows
│ ├── api/ # REST endpoints
│ └── services/ # Orchestration logic
│
├── core/ # Core configs, prompts & utilities
│ ├── settings.py
│ ├── prompts/
│ └── utils/
│
├── ingestion/ # Knowledge base ingestion pipeline
│ ├── loaders/ # Document loaders
│ ├── chunking/ # Text chunking logic
│ └── indexing/ # LlamaIndex indexing
│
├── storage/ # Vector stores & metadata storage
│ ├── vector_db/
│ └── embeddings/
│
├── .env.sample # Environment variable template
├── requirements.txt # Python dependencies
├── index.html # Optional UI / demo entry
└── README.md

yaml
Copy code

---

## 🧩 Core Components

### 🔹 Retrieval-Augmented Generation (RAG)
- Implemented using **LlamaIndex**
- Semantic indexing and retrieval of space-domain documents
- Retrieved context injected into LLM prompts to reduce hallucinations

---

### 🔹 Agentic Intelligence
- **LangChain** for tool invocation (retrieval + web search)
- **LangGraph** for orchestrating a **5-node agent workflow**:
  1. Query understanding  
  2. Knowledge retrieval  
  3. Conditional web search  
  4. Answer generation  
  5. Self-correction & validation  

Supports **conditional routing, parallel execution, and autonomy**.

---

### 🔹 Evaluation
- Evaluated using **RAGAS** framework

| Metric            | Score |
|------------------|-------|
| Context Precision | **87%** |
| Answer Relevancy  | **93%** |

Ensures objective measurement of RAG quality.

---

### 🔹 Backend & Observability
- **FastAPI** for scalable API services
- **LangSmith** for:
  - Prompt & tool-call tracing  
  - Agent decision inspection  
  - Debugging & performance tuning  

Analyzed **1000+ agent execution traces**.

---

## ⚙️ Tech Stack

- **RAG & Indexing:** LlamaIndex  
- **Agent Frameworks:** LangChain, LangGraph  
- **Evaluation:** RAGAS  
- **Backend:** FastAPI  
- **Observability:** LangSmith  

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/space_gpt.git
cd space_gpt
2️⃣ Install Dependencies
bash
Copy code
pip install -r requirements.txt
3️⃣ Configure Environment
bash
Copy code
cp .env.sample .env
# Add API keys and configuration
4️⃣ Run the Backend
bash
Copy code
uvicorn app.main:app --reload
✅ Key Outcomes
Built a production-ready Agentic RAG system

Demonstrated autonomous reasoning & self-correction

Applied evaluation-driven LLM development

Ensured reliability through full observability

📄 Declaration
This project was developed under the Space Technology Cell, ISRO & IIT Kharagpur during July–August 2025 as part of academic and research activities.

⭐ Acknowledgements
Space Technology Cell, ISRO & IIT Kharagpur

Open-source communities of LangChain, LlamaIndex, and RAGAS
