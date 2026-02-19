# n8n_projects
# Telegram AI Automation Suite (n8n)

This repository contains **three secure, credential-free n8n workflows** that turn Telegram messages into real actions using AI.

All workflows are designed to be:
- Safe to share
- Easy to import
- Credential-agnostic
- Powered by an AI Agent for intent detection

You plug in your own credentials. Nothing here spies on you. Promise.

---

## 📦 Included Workflows

### 1️⃣ Telegram AI Chat Workflow
**Purpose:**  
Responds to Telegram messages using an AI Agent with a defined personality or behavior.

**What it does:**
- Listens for incoming Telegram messages
- Sends user input to an AI Agent
- Responds back to Telegram with generated output

**Main Nodes Used:**
- Telegram Trigger
- AI Agent (LangChain)
- OpenAI Chat Model
- Telegram Send Message

**Use cases:**
- Character bots
- Smart assistants
- FAQ responders
- Fun experiments that accidentally become projects

---

### 2️⃣ Telegram Email Automation Workflow
**Purpose:**  
Handles email-related actions through Telegram using natural language.

**Supported intents:**
- 📩 Get emails
- ✉️ Send an email

**What it does:**
- Detects user intent via AI
- Fetches Gmail messages OR sends an email
- Responds back on Telegram with results

**Main Nodes Used:**
- Telegram Trigger
- AI Agent (intent-based execution)
- OpenAI Chat Model
- Gmail (Get messages)
- Gmail (Send message)
- Telegram Send Message

**Rules enforced by the agent:**
- Executes **only one action per message**
- Does not ask follow-up questions
- Does not explain internal logic

---

### 3️⃣ Telegram Calendar Reminder Workflow
**Purpose:**  
Creates Google Calendar events from Telegram messages.

**What it does:**
- Extracts date and time from natural language
- Creates exactly one calendar event
- Sets reminders correctly on the extracted date

**Time handling:**
- Uses specified time if provided
- Defaults to **9:00 AM – 10:00 AM** if no time is mentioned

**Main Nodes Used:**
- Telegram Trigger
- AI Agent
- OpenAI Chat Model
- Google Calendar (Create Event)
- Telegram Send Message

**Strict behavior:**
- One reminder per request
- No guessing
- No multi-action execution

---

## 🔐 Credentials (Not Included)

For security reasons, **no credentials are stored in this repository**.

After importing workflows into n8n, you must attach:
- Telegram Bot API credentials
- OpenAI API credentials
- Gmail OAuth credentials (for email workflow)
- Google Calendar OAuth credentials (for calendar workflow)

---

## 🚀 How to Use

1. Import the workflow JSON files into n8n
2. Attach required credentials to each node
3. Activate the workflow
4. Send commands via Telegram
5. Watch automation do its thing

---

## 🧠 Architecture Highlights

- AI-powered intent detection
- Tool-based execution (no hallucinated actions)
- Clean separation of concerns
- Shareable and production-friendly

---

## ⚠️ Notes

- Designed for **n8n + LangChain nodes**
- Tested with OpenAI chat models
- Assumes Telegram as the primary interface
- Calendar and email actions require proper OAuth scopes

---

## 📄 License

Use it. Modify it. Break it. Fix it.  
Just don’t commit credentials.

---

## ❤️ Final Thought

This repo exists because clicking buttons manually is a waste of human potential.

Automate responsibly.
