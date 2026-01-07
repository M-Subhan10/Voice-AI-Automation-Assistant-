# 🎙️🤖 Voice AI Automation Assistant

A multimodal AI voice assistant built with Gemini 2.5 Flash and LangGraph that automates productivity tasks by connecting to Google Sheets and Slack via n8n webhooks.

## 🌟 Overview

This project converts voice commands into structured actions. It records audio from the browser, uses Gemini to understand intent, and leverages a stateful LangGraph agent to decide when and how to trigger automations.

## Why This Matters

- Hands-free productivity – Log tasks and notify teams without touching a keyboard  
- Context-aware reasoning – LangGraph ensures tools are called only when needed  
- Highly extensible – n8n enables 500+ integrations (Jira, Trello, Email, etc.) with minimal changes  

## 🛠️ Tech Stack

- **LLM:** Google Gemini 2.5 Flash (Multimodal)  
- **Orchestration:** LangGraph (Agentic state machine)  
- **Automation:** n8n (Workflow automation)  
- **Environment:** Python / Google Colab  
- **Integrations:** Google Sheets API, Slack API  

## 📐 System Architecture

- **Audio Capture:** Python code in Colab records audio input  
- **Reasoning (Brain):** Gemini transcribes speech and extracts task details  
- **Routing (Logic):** LangGraph decides whether an action is required  
- **Execution (Hands):** HTTP POST request sent to an n8n Webhook  
- **Automation:** n8n logs the task in Google Sheets and sends a Slack notification  

## 🚀 Getting Started

### Prerequisites

- Google AI Studio API Key  
- n8n account (Cloud or Desktop)  
- Slack workspace with a Bot Token (`xoxb-...`)  
- Google Sheet with headers: `Timestamp`, `Task`, `Status`  

### 1️⃣ n8n Setup

- Import `n8n_workflow.json` into n8n  
- Configure Google Sheets and Slack credentials  
- Copy the Production Webhook URL  

### 2️⃣ Colab Setup

- Open the provided `.ipynb` file  
- Add API keys to environment variables / secrets  
- Paste your n8n Webhook URL into the `trigger_automation_task` function  

## 📝 Example Voice Commands

- “Add a task to call the design team tomorrow morning.”  
- “Remind me to buy coffee beans today.”  
- “Log a new task: Update the project documentation on GitHub.”  

## 📂 Repository Structure

- `Assistant_Logic.ipynb` – Main LangGraph-based assistant logic  
- `n8n_workflow.json` – n8n workflow for Sheets + Slack automation  
- `requirements.txt` – Python dependencies  

## 🤝 Contributing

Contributions are welcome!  
If you’d like to add new integrations (e.g., Google Calendar) or improve the voice recording logic, feel free to open an issue or submit a pull request.
