# 🌐 Website AI Chatbot — AI Vibz

> Conversational AI chatbot embedded on agency website — answers FAQs, captures leads, and routes interested visitors to WhatsApp for follow-up.

## 🔥 What It Does

Visitor opens website → types a message → AI responds instantly in their language → if they ask for pricing or demo → collects their WhatsApp number for follow-up. Runs 24/7 with no human needed.

## 🧠 How It Works

| Step | What Happens |
|------|-------------|
| 1 | Website sends user message + session ID to n8n webhook |
| 2 | AI Agent processes message with full conversation memory |
| 3 | Responds in same language user wrote in |
| 4 | Pricing inquiry → asks business type first |
| 5 | Demo request → asks for WhatsApp number |
| 6 | Response sent back to website in real-time |

## 🛠️ Built With

- **n8n** — webhook + workflow engine
- **OpenAI GPT-4o-mini** — AI conversation
- **Window Buffer Memory** — per-session conversation history
- **Webhook** — connects to any website frontend

## 📋 Setup

1. Import `AI_Vibz_Chatbot.json` into your n8n instance
2. Add credentials: OpenAI API
3. Copy webhook URL from n8n
4. In your website frontend — send POST request to webhook with:
```json
{
  "userMessage": "user's message here",
  "sessionId": "unique-session-id"
}
```
5. Display the text response on your site
6. Activate workflow

## 💡 Key Features

- Multilingual — auto-detects and mirrors user's language
- Per-session memory — remembers last 10 messages per visitor
- Lead capture logic built into system prompt
- Never makes up prices — always routes to WhatsApp
- Lightweight — only 5 nodes, easy to customize

## 📁 Files

| File | Description |
|------|-------------|
| `AI_Vibz_Chatbot.json` | Complete n8n workflow — ready to import |
