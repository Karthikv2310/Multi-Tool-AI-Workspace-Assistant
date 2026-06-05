# Multi-Tool AI Workspace Assistant (n8n Workflow)

An autonomous AI agent workspace built using **n8n workflow automation**. This system acts as a smart personal assistant that listens to chat interactions, handles contextual conversations via persistent memory, and executes cross-platform tasks like web searching, generating/editing Google Docs, and managing Google Calendar schedules entirely through natural language.

---

## 🚀 Key Features

* **Advanced Reasoning Engine:** Powered by an n8n `AI Agent` utilizing the **Google Gemini Chat Model** for intelligent tool selection and execution.
* **Persistent Session Memory:** Integrated with **MongoDB Chat Memory** to track context, user preferences, and session logs across conversation turns.
* **Live Search Capabilities:** Equipped with a **SerpAPI Tool** allowing the agent to fetch up-to-date information, news, and search data from the web.
* **Automated Documentation:** Deeply integrated with **Google Docs** to seamlessly generate new documents or append text to existing files based on user prompts.
* **Smart Scheduling:** Connected to **Google Calendar** to automatically create, track, and format calendar events using conversational commands.

---

## 🛠️ Workflow Architecture & Logic

![n8n Workflow Blueprint](./workflow-screenshot.png)

The execution logic follows an agentic pipeline:

1. **Trigger (`When chat message received`):** Initiates the workflow when a user interacts with the chat interface.
2. **Brain (`AI Agent`):** Processes the prompt and decides whether to respond directly or call one of its connected sub-tools.
3. **Memory Vector (`MongoDB`):** Feeds previous conversation history back into the LLM logic to ensure contextual accuracy.
4. **Toolbelt Integration:**
    * **Web Search:** `SerpAPI` fetches real-time web results.
    * **Doc Management:** `Google Docs (Create/Update)` handles text generation and file storage.
    * **Calendar Operations:** `Google Calendar (Create)` handles automatic event scheduling.

---

## 📋 Prerequisites & Environment Variables

To run this workflow, you need active accounts and API access for the following services:

| Tool / Provider | Purpose | Connection Type / Credential |
| :--- | :--- | :--- |
| **Google AI** | LLM Core (Gemini) | `Gemini API Key` |
| **MongoDB** | Contextual Chat History | `MongoDB Connection URI` |
| **SerpAPI** | Live Web Search | `SerpAPI Private Key` |
| **Google Docs** | Document Creation & Edits | `OAuth2 Google Workspace Connection` |
| **Google Calendar** | Scheduling Events | `OAuth2 Google Workspace Connection` |

---

## 🚀 Setup & Installation

1. **Clone this repository:**
   ```bash
   git clone (https://github.com/Karthikv2310/Multi-Tool-AI-Workspace-Assistant.git)
   cd Multi-Tool-AI-Workspace-Assistant
