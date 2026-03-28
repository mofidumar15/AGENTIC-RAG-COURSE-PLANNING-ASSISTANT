# 🎓 Agentic RAG Course Planning Assistant

## 📌 Overview

This project is an **Agentic Retrieval-Augmented Generation (RAG) system** designed to assist students in academic course planning using real university catalog data.

The system can:
- Check course prerequisites
- Determine eligibility for courses
- Suggest next-semester course plans
- Ask clarifying questions when student data is incomplete
- Refuse to answer when information is not available in the provided catalog (safe abstention)
- Provide citations from source documents

---

## 🧠 Key Features

- 🔍 **RAG-based Retrieval System** using Chroma vector database  
- 📚 **University Catalog Grounding** (MIT, Georgia Tech, UCSD, etc.)  
- 🤖 **Agentic Design** (Intake, Retriever, Planner, Verifier agents)  
- 🧾 **Structured Output Format** (Decision, Reasoning, Citations)  
- ❓ **Clarifying Question Handling** when student data is missing  
- ⚠️ **Safe Abstention Mechanism** (no hallucinations)  
- 📊 **Evaluation Framework with 40 test queries**

---

## 🏗️ System Architecture

1. **Data Ingestion**
   - WebBaseLoader loads university catalog pages

2. **Text Processing**
   - RecursiveCharacterTextSplitter splits documents into chunks

3. **Embeddings**
   - HuggingFace Sentence Transformers (`all-MiniLM-L6-v2`)

4. **Vector Database**
   - ChromaDB stores embeddings for retrieval

5. **Retrieval Agent**
   - Fetches relevant course/policy context

6. **Planner Agent**
   - Generates eligibility decisions and course plans

7. **Verifier Agent**
   - Validates response against retrieved context

---

## ⚙️ Installation

```bash
pip install -r requirements.txt


