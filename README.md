# 🎙️🤖 Voice AI Automation Assistant

A multimodal AI voice assistant built with Gemini 2.5 Flash and LangGraph that automates productivity tasks by connecting to Google Sheets and Slack via n8n webhooks.

## 🌟 Overview

This project converts voice commands into structured actions. It records audio from the browser, uses Gemini to understand intent, and leverages a stateful LangGraph agent to decide when and how to trigger automations.

## Why This Matters

- Hands-free productivity – Log tasks and notify teams without touching a keyboard
- Context-aware reasoning – LangGraph ensures tools are called only when needed
- Highly extensible – n8n enables 500+ integrations (Jira, Trello, Email, etc.) with minimal changes

## 🛠️ Tech Stack

LLM: Google Gemini 2.5 Flash (Multimodal)

Orchestration: LangGraph (Agentic state machine)

Automation: n8n (Workflow automation)

Environment: Python / Google Colab

Integrations: Google Sheets API, Slack API
