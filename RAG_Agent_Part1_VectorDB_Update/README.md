# RAG Agent (Part 1): Auto-Updating Vector Database from Google Drive  

**Tools:** n8n | Google Drive API | Pinecone | OpenAI Embeddings  

---

## 🎯 Overview  
This workflow automates document ingestion into a Pinecone vector database.  
Whenever a new file is uploaded to a designated Google Drive folder, the workflow automatically:  
- Detects the upload  
- Downloads the file  
- Extracts and splits the content  
- Generates embeddings using OpenAI  
- Inserts the data into Pinecone with metadata for tracking  

No manual refresh or re-upload needed — the vector database updates itself in real time.  

---

## ⚙️ Workflow Summary  

| Step | Node | Function |
|------|------|-----------|
| 1️⃣ | **Google Drive (Trigger)** | Monitors a folder (e.g., “Tesla Earnings”) for new uploads every minute |
| 2️⃣ | **Google Drive (Download)** | Downloads the newly added PDF file |
| 3️⃣ | **Document Loader** | Reads binary file data for processing |
| 4️⃣ | **Text Splitter** | Splits content into ~800-character chunks with ~50 overlap |
| 5️⃣ | **OpenAI Embeddings** | Converts text chunks into vector representations |
| 6️⃣ | **Pinecone Vector Store** | Inserts vectors into the database with metadata for file tracking |

---

## 🚀 Result  
- Fully automated document-to-vector pipeline  
- Each new Google Drive upload updates the Pinecone index automatically  
- Enables continuous knowledge updates for AI chatbots and retrieval systems  

---

## 🧠 Key Concepts  
- Event-driven automation using n8n  
- Embedding text with OpenAI for semantic search  
- Scalable vector database management in Pinecone  

---

## 🎥 Demo  
(https://www.loom.com/share/7c7dab797c934e9d9cb5ec35156e5d07)
---


**Author:** [Uday Dhanush](https://github.com/udaydhanush0207)

