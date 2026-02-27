# wonderwomen-ai-telegram-calendar-bot
Natural language to calendar automation using OpenAI, n8n, Telegram &amp; Google Calendar.# 🤖 WonderWomen AI Telegram Calendar Bot

An AI-powered Telegram bot that converts natural language messages into structured Google Calendar events using OpenAI and n8n.

## 🎯 Problem

Scheduling meetings manually from chat messages is inefficient and error-prone.  
Users often switch between messaging apps and calendar apps, causing friction and missed details.

## 💡 Solution

This bot automates the entire flow:

Natural language → Structured JSON → Calendar event creation → Telegram confirmation
---

## 🚀 What This Bot Does

Users can send messages like:

"Meeting with Preeti tomorrow at 3pm invite example@gmail.com"

The bot will:

- Extract title, date, time, duration
- Detect email attendees
- Convert natural language into structured JSON
- Create a Google Calendar event
- Send confirmation via Telegram

---
## 🧾 Sample Extracted Output

Input:
"Meeting with Preeti tomorrow at 3pm invite example@gmail.com"

Output:
{
  "title": "Meeting with Preeti",
  "date": "2026-02-28",
  "time": "15:00",
  "duration_minutes": 60,
  "attendees_emails": ["example@gmail.com"]
}

## 🧠 Tech Stack

- n8n (Workflow Automation)
- OpenAI (Natural Language Processing)
- Telegram Bot API
- Google Calendar API

---

## 🔄 Workflow Architecture

Telegram Trigger  
→ OpenAI (Task Extraction)  
→ Conditional Logic (Check Attendees)  
→ Google Calendar (Create Event)  
→ Telegram Confirmation  

---

## 📌 Key Features

- Relative date handling (today, tomorrow, weekdays)
- Default time & duration logic
- Email extraction for attendees
- Structured JSON output validation
- 24-hour time formatting

---

## 🔐 Security Note

All API credentials have been removed from this repository.  
To run this workflow, you must configure your own:

- Telegram API credentials
- OpenAI API key
- Google Calendar OAuth

---

## 🎯 Use Case

Demonstrates real-world AI automation combining NLP + workflow orchestration + calendar APIs.

---

## 📎 How to Use

1. Import `workflow.json` into n8n
2. Add your own credentials
3. Activate workflow
4. Send message to your Telegram bot

---

Built as part of an AI automation portfolio project.
