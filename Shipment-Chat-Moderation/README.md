# Real-Time AI Shipment Chat Moderation

## Overview

An AI-powered real-time moderation system designed to analyze shipment chat messages as they are received and identify abusive, offensive, or threatening content.

The system processes each incoming message independently without waiting for the conversation to end. Each message is analyzed in real time, evaluated against predefined moderation rules, and routed to the appropriate moderation action.

## Problem

Shipment conversations can contain inappropriate or abusive messages that require immediate intervention.

Manual monitoring is difficult to scale and may result in delayed responses or inconsistent moderation decisions.

## Solution

This workflow automates message-level moderation by analyzing each incoming chat message in real time and applying predefined moderation rules.

## Workflow

1. Receive an incoming shipment chat message through a webhook.
2. Normalize the incoming message data.
3. Analyze the message using AI.
4. Generate a structured moderation result.
5. Determine the violation status and severity level.
6. Trigger the appropriate moderation action.

## Key Features

- Real-time message-level analysis
- Independent processing of each incoming message
- AI-powered content moderation
- Detection of abusive, offensive, and threatening content
- Structured moderation output
- Severity classification
- Automated moderation actions

## Technologies Used

- n8n
- OpenAI API
- Webhooks
- AI-based classification
- REST APIs

## Architecture

```text
Incoming Chat Message
        |
        v
     Webhook
        |
        v
Message Normalization
        |
        v
    AI Analysis
        |
        v
Structured Output
        |
        v
Violation & Severity Decision
        |
        v
Moderation Action
