# 🤖 Telegram Personal Assistant Bot with n8n + LangChain + OpenAI

This workflow is an intelligent Telegram-based Personal Assistant powered by n8n, LangChain, OpenAI (GPT-4o), and integrations with Google Sheets, Calendar, and an Email Agent. It automates communication, contact management, and event scheduling using a natural language interface.

## ✨ Features
Chat-triggered Assistant via Telegram

OpenAI GPT-4o for conversation and decision-making

Contact verification via Google Sheets

Automated email drafting and sending

Calendar scheduling with conflict checking

Memory buffer for contextual conversations

Modular agents for email (emailAgent) and calendar (calendarAgent)

## 🔧 Architecture Overview
mermaid


Copy

Edit

graph LR

A[Telegram Trigger] --> B[LangChain Personal Assistant]

B --> C[Google Sheets - Contact Database]

B --> D[Tool: emailAgent]

B --> E[Tool: calendarAgent]

B --> F[Response via Telegram]

B --> G[OpenAI GPT-4o]

B --> H[Window Memory Buffer]


## 🧠 Workflow Breakdown
1. Telegram Trigger
Captures incoming messages from Telegram and initiates the assistant.

2. LangChain Personal Assistant
The core logic driven by a detailed system prompt. It:

Verifies contact details

Triggers email or calendar agents as required

Coordinates with tools to manage tasks in the proper order

3. Contact Database
Google Sheets integration that stores verified contact information.

4. emailAgent
A callable workflow used to draft and send emails.

5. calendarAgent
A callable workflow used to schedule meetings or events.

6. OpenAI Chat Model
Processes language understanding and generation via GPT-4o.

7. Memory Buffer
Maintains chat context per user session for coherent multi-turn interactions.

8. Response
Sends assistant replies back to the user via Telegram.

## 🛠️ Setup Instructions
Prerequisites
n8n self-hosted or cloud instance

Telegram bot token

OpenAI API key

Google Sheets & Calendar APIs enabled and authenticated in n8n

Steps
Import the workflow into your n8n instance.

Connect credentials for:

Telegram

OpenAI

Google Sheets

Set up tools:

Create emailAgent and calendarAgent workflows.

Configure your contact Google Sheet with the appropriate headers.

Activate the workflow.

Start messaging your bot in Telegram!

## 🧩 Example Usage
User Message:

"Schedule a meeting with Janvi tomorrow at 3 PM."

Assistant Response:

"Verified Alice’s contact. No scheduling conflicts. Meeting scheduled and confirmation email sent."

## 📁 Files
workflow.json – Full n8n workflow definition



## 🤝 Contributions
Pull requests are welcome. For major changes, please open an issue first.















Ch
