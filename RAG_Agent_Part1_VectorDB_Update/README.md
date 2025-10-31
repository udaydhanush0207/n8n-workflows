RAG Agent (Part 1): Auto-Updating Vector Database from Google Drive

Tools: n8n | Google Drive API | Pinecone | OpenAI Embeddings 

🎯 Overview

This workflow automates document ingestion into a Pinecone vector database.
When new files are uploaded to a Google Drive folder, the workflow automatically downloads them, processes the content, creates embeddings via OpenAI, and stores them in Pinecone — no manual updates required.

⚙️ Workflow Summary
Step	Node	Function
1️⃣	Google Drive (Trigger)	Monitors a folder (e.g., “Tesla Earnings”) for new file uploads every minute

2️⃣	Google Drive (Download)	Downloads the newly added PDF file

3️⃣	Document Loader	Reads binary file data

4️⃣	Text Splitter	Splits content into 800-character chunks with 50-character overlap

5️⃣	OpenAI Embeddings	Converts text chunks into numerical vectors

6️⃣	Pinecone Vector Store	Inserts vectors into the database with metadata for file tracking
🚀 Result

Fully automated document-to-vector pipeline

Each new Drive upload updates the Pinecone vector store automatically

Ideal for knowledge-base chatbots and dynamic retrieval systems

🧠 Key Concepts

Event-driven automation with n8n

Cloud-based vector database (Pinecone)

Embedding generation with OpenAI models (text-embedding-3-small)

Namespace and metadata management for version control
