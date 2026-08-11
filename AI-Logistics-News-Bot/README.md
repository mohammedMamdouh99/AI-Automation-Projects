# 🚚 AI Logistics News Bot

An AI-powered Telegram bot for creating, reviewing, editing, and publishing logistics news.

The workflow automates the complete news publishing lifecycle, from receiving a news item to generating the final content and image, previewing it, and publishing it to a Telegram channel.

---

## 📌 Overview

The AI Logistics News Bot is designed to simplify the process of creating and publishing logistics-related news.

Instead of manually preparing every news post, the bot provides an interactive Telegram workflow that allows the user to:

- Submit a new logistics news item
- Generate a structured news draft using AI
- Validate the generated content
- Detect duplicate news
- Request additional information when needed
- Edit and revise the draft
- Generate or reuse a suitable image
- Add branding and watermarking
- Preview the final post
- Publish the approved post to Telegram
- Cancel or restart the draft at any stage

---

## 🎯 Problem

Creating logistics news content manually requires several repetitive steps:

- Collecting the news
- Writing and formatting the article
- Checking whether enough information is available
- Detecting duplicate stories
- Creating a suitable image
- Adding branding
- Reviewing the final post
- Publishing it to the Telegram channel

This process can be time-consuming and inconsistent.

The bot automates these steps while keeping the user in control of the final publishing decision.

---

## 💡 Solution

The workflow uses n8n, Telegram, AI models, and image processing to create an end-to-end news publishing pipeline.

Each news item passes through a controlled lifecycle:

```text
Incoming Message
       ↓
Message Routing
       ↓
Draft / Edit / Publish / Cancel
       ↓
AI Draft Generation
       ↓
Content Validation
       ↓
Duplicate Detection
       ↓
Image Generation / Reuse
       ↓
Preview
       ↓
Publish
