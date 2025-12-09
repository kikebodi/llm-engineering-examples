# **LLM Engineering Examples**  
_Production-grade RAG systems, agentic workflows, evaluation pipelines, embeddings, and FastAPI integrations._

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)  
![LangChain](https://img.shields.io/badge/LangChain-%E2%9C%93-yellow)  
![Chroma](https://img.shields.io/badge/ChromaDB-%E2%9C%93-green)  
![LLM](https://img.shields.io/badge/LLM-Engineering-black)  
![FastAPI](https://img.shields.io/badge/FastAPI-%E2%9C%93-teal)  

---

## 🔍 **Overview**

This repository showcases real-world **LLM Engineering** techniques used to build reliable, auditable AI systems.  
It includes:

- **Private RAG systems** (LangChain + Chroma)  
- **Prompt engineering & optimisation**  
- **Retriever evaluation** (MRR, nDCG, keyword coverage)  
- **LLM-as-a-judge frameworks**  
- **Agentic workflows** (LiteLLM routing, orchestration patterns)  
- **Vector DB visualisation** (t-SNE 2D/3D)  
- **FastAPI endpoints for RAG/agents**  
- **Synthetic data generation** (JSONL test sets)

All examples are **production-ready** and reflect patterns used in enterprise environments.

---

## 🧠 **Architectural Diagram**

```text
                ┌─────────────────────┐
                │  Knowledge Base     │
                │  (.md, .pdf, etc.)  │
                └─────────┬───────────┘
                          │
                ┌─────────▼───────────┐
                │ Text Splitter        │
                │ (chunk_size/overlap) │
                └─────────┬───────────┘
                          │
                ┌─────────▼───────────┐
                │ Embedder (HF/OpenAI)│
                └─────────┬───────────┘
                          │ vectors
                ┌─────────▼───────────┐
                │ Vector Store (Chroma)│
                └─────────┬───────────┘
                          │ retrieve top-k
                ┌─────────▼───────────┐
                │ Retriever            │
                └─────────┬───────────┘
                          │ context
                ┌─────────▼───────────┐
                │ LLM (Chat Model)     │
                └─────────┬───────────┘
                          │ answer
                ┌─────────▼───────────┐
                │ Evaluation Layer     │
                │ (MRR, nDCG, Judge)   │
                └──────────────────────┘
```

---

## 📦 **Contents**

### **1️⃣ Basic RAG System (`rag-basic/`)**  
- End-to-end RAG built with LangChain and Chroma  
- Chunking strategy  
- Embedding pipelines  
- Persistent vectorstore  
- Retrieval + LLM pipeline  
- RAG UI using Gradio  
- Evaluation harness:
  - Mean Reciprocal Rank  
  - nDCG  
  - Keyword coverage  
  - LLM-as-judge scoring  

---

### **2️⃣ Vector DB Visualisation (`rag-visualization/`)**  
Tools to inspect embedding spaces:  
- t-SNE 2D  
- t-SNE 3D  
- Interactive Plotly visualisation  

Useful to validate semantic clustering and debug retrieval.

---

### **3️⃣ Agentic Workflows (`agentic-workflows/`)**  
Includes:  
- LiteLLM model routing  
- Multi-model orchestration  
- Task state machines  
- Agent examples  

---

### **4️⃣ FastAPI Backend (`api-fastapi/`)**  
Production endpoints for:  
- `/rag/query` → RAG answers  
- `/embed` → Embedding service  
- `/retriever/eval` → Batch evaluation  

---

### **5️⃣ Synthetic Data (`synthetic-data/`)**  
- JSONL test sets  
- Schema for question generation  
- Synthetic data generator  
- Example datasets  

---

## 🚀 **Goals**

This repository demonstrates practical, applied LLM engineering for:

- RAG systems  
- Agentic workflows  
- Embedding pipelines  
- Prompt evaluation  
- Multi-model orchestration  
- Enterprise AI architectures  

It is designed to show **depth**, **breadth**, and **real-world reliability techniques**.

---

## 📬 Contact

If you're hiring for **LLM Engineering**, **RAG systems**, **agentic workflows**, or **AI automation**, feel free to reach out.
