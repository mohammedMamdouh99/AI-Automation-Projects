<div align="center">

# 🤖 AI Automation Projects

**Real-world automation systems built with n8n, OpenAI, and AI Agents**

[![n8n](https://img.shields.io/badge/Built_with-n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)
[![OpenAI](https://img.shields.io/badge/Powered_by-OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 📌 Overview

This repository contains production-grade AI automation workflows I've built to solve real business problems. Each project is a complete, importable n8n workflow with full documentation.

> These systems are currently deployed and handling live operations at **Turbo Eg**.

---

## 📂 Projects

---

### 1. 🧠 Turbo Customer Service AI Agent
**File:** `Turbo CS Agent .json`

An enterprise-grade multi-agent customer service platform that handles customer inquiries 24/7 — automatically and intelligently.

**What it does:**
- Receives customer messages and classifies intent using AI
- Retrieves shipment status via external APIs
- Answers policy questions using a RAG knowledge base (Vector Store)
- Transcribes voice messages and analyzes images
- Auto-escalates complex cases to human agents

**Architecture:**
```
Customer Message
      │
      ▼
 Intent Classifier (OpenAI)
      │
      ├──► Shipment Tracking API
      ├──► RAG Knowledge Base (Supabase Vector Store)
      ├──► Voice Transcription
      ├──► Image Analysis
      └──► Escalation Workflow → Human Agent
```

**Tech Stack:**
`n8n` `OpenAI API` `Supabase Vector Store` `PostgreSQL` `REST APIs` `Webhooks`

---

### 2. 📧 HR Email Automation System
**File:** `HR Email Automation .json`

Eliminates manual HR email processing by automatically classifying incoming requests and extracting structured employee data.

**What it does:**
- Monitors Gmail inbox for HR-related emails
- Classifies request type (leave, complaint, onboarding, etc.)
- Extracts structured employee data from unstructured email content
- Logs everything to Google Sheets automatically

**Flow:**
```
Incoming Email (Gmail)
      │
      ▼
 AI Classification (OpenAI)
      │
      ▼
 Data Extraction → Google Sheets
```

**Tech Stack:**
`n8n` `OpenAI API` `Gmail API` `Google Sheets API`

---

### 3. 💬 Technical Support Chatbot (Telegram)
**File:** `TechnicalSupportTurboBot .json`

An AI-powered Telegram bot that handles internal IT support requests — collecting, classifying, and logging them automatically.

**What it does:**
- Receives support requests via Telegram
- Guides users through structured input collection
- Classifies request type using AI
- Logs tickets to Google Sheets with full details

**Flow:**
```
User Message (Telegram)
      │
      ▼
 Structured Input Collection
      │
      ▼
 AI Classification → Google Sheets Log
```

**Tech Stack:**
`n8n` `Telegram Bot API` `OpenAI API` `Google Sheets API`

---

### 4. 📰 AI Logistics News Automation
**File:** `Logistics News.json`

Automates logistics industry monitoring — collecting, filtering, and summarizing news using AI.

**What it does:**
- Pulls logistics news from multiple API sources
- Filters for relevance using AI classification
- Generates structured summaries and insights
- Delivers formatted reports automatically

**Flow:**
```
News APIs (HTTP)
      │
      ▼
 Relevance Filter (AI)
      │
      ▼
 AI Summary Generation → Structured Report
```

**Tech Stack:**
`n8n` `OpenAI API` `HTTP Request` `RSS Feeds`

---

## 🚀 How to Use

1. Download the `.json` file for the workflow you want
2. Open your n8n instance
3. Go to **Workflows → Import from File**
4. Upload the `.json` file
5. Configure your credentials (API keys, Gmail, Telegram, etc.)
6. Activate the workflow

---

## 🛠 Prerequisites

- [n8n](https://n8n.io) (self-hosted or cloud)
- OpenAI API key
- Relevant API credentials per workflow (Gmail, Telegram, Supabase, etc.)

---

## 👤 Author

**Mohamed Mamdouh Ismail** — AI & Automation Specialist

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/mohamed-mamdouh-ai/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mohammeddo7aa@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/mohammedMamdouh99)

---

<div align="center">

⭐ If these workflows helped you, consider giving the repo a star!

</div>
