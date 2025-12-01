# RAG Agent (Part 2): AI Agent, Vector Search & Retrieval Pipeline

**Tools:** n8n | Pinecone | OpenAI GPT-4 | Google Drive | Embeddings

---

## 🎯 Overview
This workflow transforms the auto-updating Pinecone vector database (from Part 1) into a fully functional **Retrieval-Augmented Generation (RAG) AI Agent**.

Whenever a user submits a question, the agent:
- Performs **vector search** in Pinecone
- Retrieves the most relevant document chunks
- Generates an answer grounded in the uploaded PDF files

This ensures responses are **accurate, contextual, and document-based** rather than hallucinated.

---

## ⚙️ Pipeline Summary

| Step | Node | Action |
|------|------|--------|
| 1️⃣ | Webhook / UI Input | Accepts user question |
| 2️⃣ | Pinecone: Query Vector Store | Performs vector search on embedded documents |
| 3️⃣ | OpenAI Embeddings | Converts user query into embedding vector |
| 4️⃣ | Context Builder | Merges top-k chunks into a single prompt |
| 5️⃣ | OpenAI Chat Completion | Generates final grounded answer |

---

## 🧠 Key Concepts

- **Vector Search** → Retrieves semantically similar chunks from Pinecone  
- **Embeddings** → Map text into numerical vectors for similarity comparison  
- **RAG Prompt** → Combines retrieved chunks with the user’s query  
- **LLM Answer** → Grounded in uploaded documents, minimizing hallucinations  
- **n8n Agent Node** → Functions as a fully automated Q&A system  

---

## 🚀 Final Output

- Answers questions based on **PDF uploads**  
- Knowledge base updates **automatically** (from Part 1 pipeline)  
- Provides **accurate, document-grounded insights**  
- Ready for deployment as:  
  - Web chatbot  
  - Helpdesk bot  
  - Internal knowledge tool
