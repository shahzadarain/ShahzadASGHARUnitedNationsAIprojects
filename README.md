# BoolyAI: Secure Multi-Modal AI Assistant

![Status](https://img.shields.io/badge/Status-Production-success)
![Stack](https://img.shields.io/badge/Stack-Python_%7C_Azure_AI_%7C_WhatsApp-blue)
![Type](https://img.shields.io/badge/Category-Agentic_AI-orange)

> **⚠️ Note:** This repository serves as the public documentation and architectural overview for **BoolyAI**. The source code is currently private/internal.

## 🚀 Project Overview
**BoolyAI** is an agentic AI assistant designed to bridge the gap between Large Language Models (LLMs) and everyday communication. Operating natively within WhatsApp, it acts as a secure "pocket companion" capable of processing voice, text, and images.

It was built to solve the challenge of accessibility—bringing high-power AI tools to users in a low-friction environment without requiring new app installations.

## 🏗️ Architecture

```mermaid
graph TD
    User((User)) -->|WhatsApp Voice/Text| WAPI[WhatsApp Cloud API]
    WAPI -->|Webhook| Gateway[API Gateway]
    Gateway -->|Secure Payload| Core[Booly Core Engine / Python]
    
    subgraph "AI Processing Layer"
        Core -->|Audio| Whisper[Whisper Model STT]
        Core -->|Image| Vision[Computer Vision / OCR]
        Core -->|Text| LLM[LLM Inference Engine]
    end
    
    subgraph "Memory & Context"
        Core <--> DB[(Vector DB / User Context)]
    end
    
    LLM -->|Response| Core
    Core -->|Formatted Msg| WAPI
    WAPI -->|Reply| User


✨ Key Capabilities
Multi-Modal Inputs: Seamlessly understands text, voice notes (audio), and images.

Persistent Memory: Maintains conversation context across sessions for a personalized experience.

RAG (Retrieval-Augmented Generation): Connects to external knowledge bases to provide factual, grounded answers.

Document Intelligence: Users can upload photos of documents for instant OCR and summarization.

🛠️ Tech Stack
Core Backend: Python

AI Services: Azure OpenAI Service, Whisper (Speech-to-Text)

Integration: Meta (WhatsApp) Graph API

Data: PostgreSQL & Vector Stores

Deployment: Dockerized Microservices

Created by Shahzad Asghar


***

### 2. DAGREQ Readme
*Create a repository named `dagreq-platform` (or similar), create a file named `README.md`, and paste this:*

```markdown
# DAGREQ: Enterprise Service Request Management Platform

![Status](https://img.shields.io/badge/Status-Live-success)
![Focus](https://img.shields.io/badge/Focus-Workflow_Automation-blueviolet)
![Scale](https://img.shields.io/badge/Scale-Enterprise-critical)

> **⚠️ Note:** This repository serves as the technical portfolio for the **DAGREQ** system. The source code is proprietary.

## 📖 Executive Summary
**DAGREQ** is a specialized Service Request Management System designed to eliminate operational bottlenecks in complex organizations. It replaces disjointed email chains and spreadsheets with a centralized, tracked, and automated digital pipeline.

The system was architected to handle high-volume service requests with strict **SLA (Service Level Agreement)** tracking, ensuring transparency and accountability.

## ⚡ The Solution

| The Challenge | The DAGREQ Solution |
| :--- | :--- |
| **Fragmented Requests** | A "Single Pane of Glass" portal for all incoming tickets. |
| **Invisible Bottlenecks** | Real-time dashboards showing "Time to Resolution" metrics. |
| **Manual Routing** | Intelligent auto-assignment based on request type and load. |
| **Audit Compliance** | Full history tracking of every action and approval. |

## ⚙️ Core Modules
1.  **Dynamic Form Engine:** Allows admins to create custom request types without code changes.
2.  **Workflow Orchestrator:** Manages state transitions (Draft $\rightarrow$ Approval $\rightarrow$ In Progress $\rightarrow$ Done).
3.  **Analytics Dashboard:** Visualizes team performance, peak request times, and backlog trends.
4.  **Notification Hub:** Automated alerts via Email and instant messaging integrations.

## 💻 Technical Highlights
* **Architecture:** Modular Monolith (Designed for Microservices migration).
* **Frontend:** Modern Responsive Web App.
* **Backend:** Python.
* **Database:** ACID-compliant relational design for strict data integrity.
* **Security:** Role-Based Access Control (RBAC) and SSO integration.

---
*Created by [Shahzad Asghar](https://www.linkedin.com/in/shahzadasghar-ai/))*
