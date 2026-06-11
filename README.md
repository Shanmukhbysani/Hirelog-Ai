# HireLog Placement Archive

<p align="center">
  <strong>Transform Interview Experiences into Searchable Placement Intelligence</strong>
</p>

<p align="center">
  A full-stack platform that helps students document, discover, and learn from real interview experiences through AI-powered search and analytics.
</p>

---

## 🚀 Live Applicationn

Frontend Deployment:  
https://hirelogapp.vercel.app/

---

## 📖 Overview

HireLog is a centralized placement knowledge platform designed to capture interview experiences and convert them into structured, searchable institutional knowledge.

Instead of valuable interview insights getting lost in chats and spreadsheets, HireLog enables students to contribute experiences that can be enriched using NLP techniques and retrieved through intelligent search.

The platform combines:

- Structured experience collection
- AI-powered content enrichment
- Hybrid search (vector + lexical)
- Placement analytics
- Practice question tracking
- Moderation and dashboard tools

---

## ✨ Key Features

### 📝 Interview Experience Archive
- Submit interview experiences using structured forms
- Store company, role, rounds, questions, outcomes, and insights
- Maintain a growing institutional placement repository

### 🤖 AI-Powered Enrichment
- Automatic topic extraction
- Interview question identification
- Content summarization
- Embedding generation for semantic search

### 🔍 Intelligent Search
- Hybrid retrieval architecture
- Semantic vector search
- Lexical keyword matching
- Re-ranking pipeline for relevance optimization

### 📊 Analytics Dashboard
- Placement trend analysis
- Company-wise insights
- Experience moderation tools
- Search and engagement metrics

### 📚 Practice & Preparation
- Question tracking
- Practice lists
- Frequently asked interview questions
- Topic-based preparation workflows

---

## 🏗️ Architecture

text Frontend (Next.js)         │         ▼ FastAPI Backend         │         ├── Firebase Authentication         ├── Firestore Database         ├── NLP Processing Pipeline         ├── Embedding Generation         └── Search & Ranking Engine 

---

## 📂 Repository Structure

text . ├── backend/ │   ├── app/ │   ├── scripts/ │   ├── tests/ │   └── Dockerfiles │ ├── frontend/ │   ├── app/ │   ├── components/ │   ├── contexts/ │   └── tests/ │ └── docs/     ├── deployment guides     ├── engineering standards     └── operational runbooks 

---

## 🛠️ Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- Firebase Authentication

### Backend
- FastAPI
- Python
- Firebase Admin SDK
- Firestore

### AI & Search
- NLP Processing Pipeline
- Embeddings
- Semantic Search
- Hybrid Retrieval & Re-ranking

### Deployment
- Vercel (Frontend)
- Hugging Face Docker Space (Backend)

---

## 🚀 Local Development

### Backend Setup

bash cd backend  python -m venv .venv  # Windows .venv\Scripts\Activate.ps1  pip install -r requirements.txt pip install -r requirements-dev.txt  cp .env.example .env  uvicorn app.main:app --reload --port 8000 

Backend will be available at:

text http://localhost:8000 

---

### Frontend Setup

bash cd frontend  npm install  cp .env.example .env.local  npm run dev 

Frontend will be available at:

text http://localhost:3000 

---

## ⚙️ Environment Variables

### Backend

Use:

text backend/.env.example 

Required:

text FIREBASE_PROJECT_ID FIREBASE_SERVICE_ACCOUNT_PATH # or FIREBASE_SERVICE_ACCOUNT_JSON  ALLOWED_ORIGINS 

---

### Frontend

Use:

text frontend/.env.example 

Required:

text NEXT_PUBLIC_API_BASE_URL  NEXT_PUBLIC_FIREBASE_API_KEY NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN NEXT_PUBLIC_FIREBASE_PROJECT_ID  NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID NEXT_PUBLIC_FIREBASE_APP_ID 

---

## 🚢 Deployment

### Frontend

Deployed on Vercel:

https://hirelogapp.vercel.app/

### Backend

Deployed independently on a Hugging Face Docker Space.

Deployment Guide:

text docs/backend-deployment.md 

### Deployment Workflow

1. Configure Hugging Face Space credentials
2. Configure Firebase environment variables
3. Deploy backend
4. Verify health endpoints
5. Update frontend API URL

Health checks:

text /health /health/live /health/ready /health/deep 

---

## 🔌 API Endpoints

### Public Endpoints

text GET / GET /health GET /health/live GET /health/ready GET /health/deep  GET /api/search GET /api/search/facets 

### Authenticated Endpoints

text /api/users/* /api/experiences/* /api/practice-lists/* /api/dashboard/* 

---

## ✅ Quality Gates

### Backend

bash cd backend  .venv\Scripts\python.exe -m ruff check . .venv\Scripts\python.exe -m pytest .venv\Scripts\python.exe -m compileall app 

### Frontend

bash cd frontend  npm run lint npm run type-check npm run test:ci npm run build npm run test:e2e 

---

## 📚 Documentation

text docs/backend-deployment.md docs/backend-cutover-runbook.md docs/engineering-standards.md 

---

## 🔒 Security

- Service account credentials are never committed to source control.
- Firestore access rules are defined in firestore.rules.
- Backend operations use Firebase Admin SDK.
- Environment secrets are managed separately from application code.

---

## 🎯 Vision

HireLog aims to become a placement intelligence platform where every interview experience contributes to a continuously growing knowledge base, helping future candidates prepare smarter and perform better.

---

Built to make placement preparation data-driven, searchable, and collaborativ
