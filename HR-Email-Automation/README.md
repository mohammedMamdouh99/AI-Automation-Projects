# 📧 HR Email Automation

An AI-powered HR email processing workflow built with **n8n, Gmail, OpenAI, Google Sheets, and Turbo**.

The system monitors incoming HR emails, validates and classifies requests using AI, routes them to the appropriate automated process, and creates structured tasks for internal operations.

---

## 📌 Overview

HR teams receive different types of requests through email, often containing unstructured information that requires manual review, classification, and follow-up.

This automation transforms the email-based process into a structured workflow by:

- Monitoring incoming HR emails
- Identifying new HR requests
- Filtering relevant emails
- Classifying requests using AI
- Extracting structured information
- Routing requests to the correct process
- Creating tasks in the internal task management system
- Generating standardized email responses
- Storing selected structured data for reporting

---

## 🎯 Problem

Processing HR requests manually can lead to:

- Repetitive administrative work
- Inconsistent request classification
- Delayed task creation
- Manual data extraction
- Inconsistent communication
- Difficulty tracking different HR request types

The automation reduces these manual steps and standardizes the process.

---

## 💡 Solution

The workflow acts as an AI-powered processing layer between the HR mailbox and internal operational systems.

Each incoming request follows an automated pipeline:

```text
Incoming HR Email
        ↓
Email Validation
        ↓
New Request Check
        ↓
Turbo Email Filter
        ↓
AI Classification
        ↓
Request-Specific Routing
        ↓
Data Extraction
        ↓
Task Creation / Google Sheets
        ↓
Automated Email Response
