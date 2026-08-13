# Customer Service Ticket Quality & Classification

An AI-powered customer service quality evaluation and ticket classification
workflow built with n8n.

## Overview

This workflow processes customer service tickets and performs two AI-driven
tasks in parallel:

1. Evaluates the quality of the customer service agent's communication.
2. Classifies the customer service ticket based on the customer's actual need.

The workflow receives ticket data through a webhook, prepares and analyzes
the ticket conversation, then sends the processed data to two independent
AI agents.

---

## Workflow Architecture

The workflow follows two parallel AI processing branches:

```text
                         Webhook
                            ↓
                       Edit Fields
                            ↓
                  Code in JavaScript
                       /          \
                      /            \
                     ↓              ↓
             Quality Agent    Ticket Classification Agent
                     ↓              ↓
             Score Calculator   Classification Parser
                     ↓              ↓
              Google Sheets     Google Sheets
                     \              /
                      \            /
                       ↓          ↓
                    Respond to Webhook
                            ↓
                    Execution Data
