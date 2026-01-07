#Voice-AI-Automation-Assistant-🎙️🤖
A multimodal AI voice assistant built with Gemini 2.5 Flash and LangGraph that automates productivity tasks by connecting to Google Sheets and Slack via n8n webhooks.

🌟 Overview
This project transforms verbal commands into structured data and automated actions. It captures audio from the browser, uses Gemini to understand the intent, and employs a stateful LangGraph agent to decide when and how to trigger external automations.

Why this matters:
Hands-free Productivity: Log tasks and notify teams without touching a keyboard.

Context-Aware: Uses LangGraph to maintain state and ensure tools are only called when necessary.

Extensible: The n8n backend allows for adding 500+ other integrations (Jira, Trello, Email) with minimal code changes.

🛠️ Tech Stack
LLM: Google Gemini 2.5 Flash (Multimodal processing)

Orchestration: LangGraph (Agentic state machine)

Automation: n8n (Workflow automation engine)

Environment: Google Colab / Python

Integrations: Google Sheets API, Slack API

📐 System Architecture
Audio Capture: Python code in Colab records audio and sends it to Gemini.

Reasoning (The Brain): Gemini transcribes and extracts "Task Details."

Routing (The Logic): LangGraph checks if the output requires an action.

Execution (The Hands): An HTTP POST request is sent to an n8n Webhook.

Automation: n8n simultaneously appends a row to Google Sheets and pings a Slack channel.

🚀 Getting Started
Prerequisites
A Google AI Studio API Key.

An n8n account (Cloud or Desktop).

A Slack Workspace (with a Bot Token xoxb-...).

A Google Sheet with headers: Timestamp, Task, Status.

1. n8n Setup
Import the workflow.json (found in this repo) into n8n.

Set your Google Sheets and Slack credentials.

Copy your Production Webhook URL.

2. Colab Setup
Open the provided .ipynb file.

Add your API keys to the Secrets/Environment variables.

Paste your n8n Webhook URL into the trigger_automation_task tool function.

📝 Example Commands
"Add a task to call the design team tomorrow morning."

"Remind me to buy coffee beans today."

"Log a new task: Update the project documentation on GitHub."

📂 Repository Structure
Assistant_Logic.ipynb: The main Python notebook containing the LangGraph logic.

n8n_workflow.json: The exported n8n workflow file for easy import.

requirements.txt: Python dependencies.

🤝 Contributing
Contributions are welcome! If you'd like to add new tools (like a Calendar integration) or improve the voice recording logic, please open an issue or a PR.
