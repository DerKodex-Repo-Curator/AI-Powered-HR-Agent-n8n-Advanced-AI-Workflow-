# AI-Powered-HR-Agent-n8n-Advanced-AI-Workflow-
An autonomous AI Agent built within n8n to automate Human Resources operations, manage employee inquiries, filter candidate resumes, and streamline HR internal workflows using LLMs.
## 🎯 Problem Solved
HR departments spend hours answering repetitive employee questions (e.g., policy details, vacation balances, onboarding steps) and manually screening job applications. 

This workflow deploys an **AI Agent** equipped with custom tools and memory. It acts as a first-line HR assistant that can understand natural language, reference internal company policies, and interact with external HR systems or databases to process requests autonomously.

---

## ⚡ Agent Architecture
User / Employee Inquiry (Text)
             ↓
   n8n AI Agent Executor
             ↓
┌────────────┼────────────┐
↓            ↓            ↓
[Memory]    [HR Vector]   [Custom Tools]
(Context)   (Policies)    (ERP / DB Actions)
└────────────┬────────────┘
↓
Autonomous Response


---

## 🔧 Tech Stack
| Tool | Role |
| :--- | :--- |
| **n8n Advanced AI** | Agent orchestration and tool calling framework |
| **OpenAI / Anthropic** | The LLM brain powering the agent's reasoning |
| **Vector Store (Pinecone/Qdrant)** | Semantic search for company handbook & HR policies |
| **Odoo / HR Database** | Custom tools connected to the agent to read/write employee data |

---

## 📋 Capabilities & Agent Tools
The HR Agent is configured with specialized capabilities:
* **💬 Policy Q&A:** Connected to a knowledge base to answer complex questions about company guidelines instantly.
* **📅 Leave Management Tool:** Allows the agent to look up vacation balances or draft time-off requests directly in the HR system.
* **📂 Employee Directory Lookup:** Dynamically retrieves basic employee metadata for personalized interactions.

---

## 🚀 Setup Instructions

### Prerequisites
* n8n instance (Self-hosted or Cloud) with **Advanced AI** nodes enabled.
* API Key from an LLM provider (OpenAI, Anthropic, or Ollama for local models).
* Vector Database credentials or connected local memory.

### Steps to Deploy
1.  **Import:** Download and import `HR_Agent_Template.json` into your n8n canvas.
2.  **Configure LLM:** Open the Model node and insert your OpenAI/Anthropic credentials.
3.  **Link Knowledge Base:** Connect your preferred vector store or text file containing your HR policies to the retrieval tool.
4.  **Connect Tools:** Update the custom HTTP/Code tools inside the agent to point to your actual HR software or Odoo instance API.
5.  **Test:** Use the built-in n8n chat interface to talk to your new HR Agent live.

---

## 📁 Repository Structure
```bash
ai-hr-agent/
├── HR_Agent_Template.json         # The clean n8n AI Agent workflow file (Import this)
├── agent-chat-interface.png       # Screenshot of the n8n AI chat interface
└── README.md                      # Project documentation
👤 Author
Asem Ahmed — AI Automation Engineer 

Specializing in Multi-Agent systems, Enterprise Automation, and LLM integrations.

