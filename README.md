# n8n-agent-for-google-calendar-automation (Telegram + Google Calendar + OpenAI)

An AI-powered calendar assistant built using **n8n**, that lets you manage your **Google Calendar** directly from **Telegram** using natural language commands.
Supports creating, updating, deleting, and listing events — powered by **OpenAI GPT model** and Google Calendar APIs.

## Features

* **Manage Calendar via Telegram**

  * Create events
  * Update events
  * Delete events
  * Get upcoming events
* **AI Agent Powered by OpenAI GPT**

  * Understands your text commands (e.g., *"Create a meeting tomorrow at 5 PM"*).
  * Smartly picks the right calendar operation.
* **Memory Buffering**

  * Retains session context for smoother conversations.
* **Google Calendar Integration**

  * Works with your personal or business calendar.
*  **Supports Both Text & Audio Input** (Detects if you send voice message)

## 🛠️ Tech Stack

* **n8n** (Workflow Automation)
* **Telegram Bot API**
* **Google Calendar API**
* **OpenAI GPT (gpt-4o-mini model)**
* Langchain AI Agent + Memory
* No-code, Low-code solution with scalable node-based workflow

## Setup Instructions

1. **Clone This Workflow**

Download or clone this n8n workflow JSON and import into your n8n instance.

2. **Connect Your APIs**

* Set up credentials for:

  * **Telegram Bot** (get token from [@BotFather](https://t.me/botfather))
  * **Google Calendar OAuth** connection
  * **OpenAI API Key** (or use free credits in n8n)

3. **Deploy & Run**

* Make sure your n8n instance is publicly accessible for **Telegram Webhooks**.
* Activate the workflow.
* Start chatting with your bot on Telegram!


## Commands You Can Try

| Command                           | Result                  |
| --------------------------------- | ----------------------- |
| "Create meeting tomorrow at 5 PM" | Creates new event       |
| "Delete event with ID xyz"        | Deletes specified event |
| "Update event xyz to 6 PM"        | Updates event timing    |
| "Show my events next week"        | Lists upcoming events   |


## Nodes & Logic Overview

* **Telegram Trigger** ➔ Listens for new messages
* **Switch Node** ➔ Detects if message is Text or Audio
* **Set Node** ➔ Prepares message text
* **AI Agent (Langchain)** ➔ Reads user intent and picks correct tool:

  * Create event
  * Update event
  * Delete event
  * GetAll events
* **Google Calendar Tool** ➔ Executes the calendar operation
* **Memory Buffer Node** ➔ Stores session context per user
* **OpenAI Node** ➔ LLM backend (GPT-4o-mini)

## Requirements

* n8n instance (self-hosted or cloud)
* Telegram Bot
* Google Calendar
* OpenAI API Key

## Connect with me

* **Suravi S Thatha**
  [LinkedIn](https://www.linkedin.com/in/suravi-s-thatha/) | [Portfolio](https://suravi-s-thatha.vercel.app)
