# Event-intelligence-rag-system
Retrieval-Augmented Generation (RAG) system for operational event intelligence using alarm and incident data (Fire, EMS, Civil Defence) using embeddings and vector search.

## Overview
This project implements a **Retrieval-Augmented Generation (RAG) system** for operational event intelligence.  
It enables natural language querying over alarm and incident data related to **Fire, EMS, and Civil Defence operations**.

The system ingests structured incident data, transforms it into rich textual narratives, stores semantic embeddings in a vector database, and retrieves context-aware answers using an LLM.

---

## Business Use Case
Operational teams often struggle to quickly extract insights from large volumes of alarm and incident data.  
This RAG system allows users to ask questions such as:

- "Why are there so many critical alarms from component 103?"
- "What SOP steps were followed for incident INC020147?"
- "How many water leakage incidents occurred last week?"

The system responds using **only the retrieved operational context**, ensuring grounded and reliable answers.

---

## Architecture
**Pipeline Flow:**

1. CSV Ingestion → Relational Database (SQLite)
2. Feature Engineering → Human-readable event narratives
3. Intelligent Text Chunking
4. Embedding Generation (Open-source model)
5. Vector Storage (Chroma / Qdrant / Milvus)
6. Semantic Retrieval (Top-K)
7. LLM-based Answer Generation (RAG)

---

## Dataset
- **Source:** Operational alarm & incident platform
- **Format:** CSV
- **Sample Fields:**
  - ALARM_ID
  - PRIORITY
  - COMPONENT_ID
  - ALARM_GENERATED_TIME
  - SECONDARY_AGENCY
  - BPM_ESCULATION_COUNT
  - SEVERITY
  - URGENCY
  - SOP_DOCUMENT_URL

---

## Tech Stack
- **Language:** Python
- **Database:** SQLite
- **Vector DB:** Chroma / Qdrant (pluggable)
- **Embeddings:** Open-source embedding model (e.g., BGE-M3)
- **LLM:** Any compatible LLM (OpenAI / Open-source)
- **Frameworks:** LangChain / Custom RAG pipeline

---

## Project Structure

