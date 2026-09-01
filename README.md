# 🤖 AI Study Assistant

An AI-powered study assistant built using **n8n, Google Gemini, Supabase, RAG, and Gmail Automation**.

The system allows users to ask questions about their personal study notes through email. It uses **Retrieval-Augmented Generation (RAG)** to search relevant information from stored notes and generate intelligent responses.

---

## 🚀 Features

- 📚 Store personal study notes in a vector database
- 🔍 Semantic search using vector embeddings
- 🤖 AI-powered question answering using Google Gemini
- 🧠 RAG (Retrieval-Augmented Generation)
- 📧 Ask questions through Gmail
- ✉️ Automatically send AI-generated responses via email
- 💬 Conversation memory using n8n AI Memory
- ⚙️ Fully automated workflows using n8n
- 🗄️ Supabase PostgreSQL with pgvector

---

## 🏗️ Architecture

### Workflow 1: Notes Ingestion

```text
Study Notes
    ↓
Manual Trigger
    ↓
Edit Fields
    ↓
Document Loader
    ↓
Text Splitter
    ↓
Gemini Embeddings
    ↓
Supabase Vector Store

2nd workflow

User Email
    ↓
Gmail Trigger
    ↓
AI Agent
    ├── Google Gemini Chat Model
    ├── Simple Memory
    └── Supabase Vector Store
            ↓
       Search Notes
            ↓
        AI Response
            ↓
      Gmail Send Message
