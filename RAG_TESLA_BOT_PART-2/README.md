# RAG Agent (Part 2): AI Agent, Vector Search & Retrieval Pipeline

**Tools:** n8n | Pinecone | OpenAI GPT-4 | Google Drive | Embeddings

---

## 🎯 Overview
This workflow transforms the auto-updating Pinecone vector database (from Part 1) into a fully functional **Retrieval-Augmented Generation (RAG) AI Agent**.

<img width="3200" height="1662" alt="image" src="https://github.com/user-attachments/assets/9d4d7c0b-5533-4cd3-9e9a-748d4021d6f6" />

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

<img width="3196" height="1666" alt="image" src="https://github.com/user-attachments/assets/bc8ec4dd-7a63-4f69-85c9-666199284b90" />


- Answers questions based on **PDF uploads**  
- Knowledge base updates **automatically** (from Part 1 pipeline)  
- Provides **accurate, document-grounded insights**  
- Ready for deployment as:  
  - Web chatbot  
  - Helpdesk bot  
  - Internal knowledge tool
