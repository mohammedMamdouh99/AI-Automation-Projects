# AI Customer Service Ticket Agent

AI-powered customer service ticket processing workflow built with n8n.

## Overview

This project automates the processing of customer service tickets using
multimodal input processing, AI planning, controlled tool execution,
knowledge retrieval, and escalation handling.

The workflow supports text, image, voice, and file inputs before routing
the request through the appropriate AI processing path.

## Architecture

The workflow is structured around the following stages:

1. Customer input
2. Authentication
3. Input type detection
4. Multimodal processing
5. AI-enabled decision
6. AI planning
7. Customer Service Agent execution
8. Knowledge retrieval and operational tools
9. Escalation handling
10. Execution data

## AI Planning

The workflow uses a dedicated Planner Agent to determine which tools are
required to handle a customer request.

The Planner produces a structured tool plan before the Customer Service
Agent executes the required tools.

## Customer Service Agent

The Customer Service Agent L1 can use the following tools:

- VectorStore
- ShipmentInfo
- MissionInfo
- BranchInfo
- NoAnswer
- DelayedShipment
- UrgentShipment
- CoveragesInfo

## Knowledge Retrieval

The workflow includes a VectorStore connected to:

- OpenAI Embeddings
- Cohere Reranker

This provides the Customer Service Agent with a retrieval-based knowledge
source for supported customer service queries.

## Multimodal Processing

The workflow supports multiple input types:

- Text
- Images
- Voice
- Files

Voice inputs are transcribed before being passed to the AI processing flow.
Images and files are processed through dedicated OpenAI processing nodes.

## Escalation

The workflow includes a separate escalation detection path.

Escalation can be triggered by the AI decision or by repeated messages
within a defined time window.

When escalation is required, the workflow sends the ticket to the
escalation endpoint before continuing to the execution stage.

## Technologies

- n8n
- OpenAI
- PostgreSQL Chat Memory
- Vector Store
- Cohere Reranker
- Turbo Platform API

## Workflow

The exported n8n workflow is available in:

`Workflow.json`

## Documentation

Detailed architecture documentation and workflow diagrams will be added
under the `docs/` directory.

## Security

The workflow file included in this repository is a sanitized version.
Credentials, passwords, and sensitive authentication values are not
included.

Never commit API keys, passwords, tokens, or private credentials to the
repository.
