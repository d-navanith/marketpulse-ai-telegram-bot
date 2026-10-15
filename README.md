# 📈 MarketPulse AI — Daily Financial Briefing Telegram Bot

An autonomous end-to-end AI automation pipeline built with **n8n**, **Google Gemini**, and the **Telegram Bot API**. 

The system wakes up automatically every morning, ingests live world currency exchange rates, generates a concise executive financial briefing using Google Gemini, and delivers it straight to Telegram.

---

## 🏗️ Architecture

[⏰ Schedule Trigger (8:00 AM)] │ ▼ [🌐 HTTP Request (Live Forex API)] │ ▼ [🧠 Basic LLM Chain + Google Gemini AI] │ ▼ [📲 Telegram Bot (@finbrief_update_bot)]


---

## ⚡ Features
* **Autonomous Daily Execution:** Runs on a scheduled cron trigger at 8:00 AM without manual intervention.
* **Real-Time Data Ingestion:** Connects to live currency exchange REST APIs to fetch up-to-the-minute global forex rates.
* **AI-Powered Synthesis:** Prompts Google Gemini Flash to act as a financial analyst and extract executive-level insights on major currencies (USD, EUR, GBP, JPY, AUD).
* **Mobile & Desktop Push Alerts:** Formats and dispatches updates directly to a personal or team Telegram channel.

---

## 🚀 How to Import & Run in n8n

1. Clone or download **`workflow.json`** from this repository.
2. Open your **n8n instance** (`http://localhost:5678`).
3. Click the **three dots (`...`)** in the top-right corner of the canvas ➔ **Import from File**.
4. Select `workflow.json`.
5. Configure your credentials:
   * **Google Gemini API:** Add your free API key from [Google AI Studio](https://aistudio.google.com/).
   * **Telegram API:** Enter your bot token from `@BotFather` and your chat ID.
6. Click **Publish** to start your automated daily briefings!

---

## 🛠️ Tech Stack
* **Workflow Engine:** n8n (Self-hosted)
* **LLM:** Google Gemini 3 Flash / 1.5 Flash
* **API Ingestion:** Open Exchange Rates REST API
* **Messaging:** Telegram Bot API
