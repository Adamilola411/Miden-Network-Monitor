# Miden Network Health Monitor 🛡️

A lightweight, "future-ready" observability tool designed for the **Miden Network**. This project uses GitHub Actions to monitor Miden RPC endpoints and client-side performance, sending real-time alerts directly to **Telegram**.

## ✨ Features
* **9-Minute Heartbeat:** Automated status checks using GitHub Cron schedules.
* **Zero-Cost Infrastructure:** Runs entirely on GitHub Actions (no paid servers needed).
* **Instant Alerts:** Immediate Telegram notifications for node downtime or RPC failures.
* **Miden-Specific:** Tailored to track the unique "Edge Blockchain" architecture of @0xmiden.

## 🛠️ Setup Instructions

### 1. Telegram Bot Configuration
1.  Message [@BotFather](https://t.me/botfather) to create a bot and get your **API Token**.
2.  Get your **Chat ID** using [@userinfobot](https://t.me/userinfobot).
3.  Start a chat with your bot.

### 2. GitHub Secrets
Add the following secrets in **Settings > Secrets and variables > Actions**:
* `TELEGRAM_TOKEN`: Your Bot API Token.
* `TELEGRAM_TO`: Your Telegram Chat ID.

### 3. Installation
1.  Fork or clone this repository.
2.  The monitor is located in `.github/workflows/miden_monitor.yml`.
3.  (Optional) Edit the RPC URL in the YAML file to point to your specific node.

## 📊 How it Works
The monitor pings the Miden RPC every 9 minutes. If the network returns anything other than a `200 OK` or fails to respond, the workflow triggers a failure state and the Telegram bot sends an alert with a direct link to the logs.

## 🤝 Contributing
Feel free to open issues or pull requests to add metrics like:
* Note consumption latency tracking.
* Miden VM memory usage logs.
* Airdrop reward tracking integration.

---
**Built for the @0xmiden Ecosystem**
