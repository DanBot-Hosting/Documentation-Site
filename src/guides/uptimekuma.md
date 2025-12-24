---
order: 50
icon: pulse
title: Installing Uptime Kuma
---

# Installing Uptime Kuma

Uptime Kuma is a self-hosted monitoring tool. Follow the steps below to install it on your AIO server.

---

## Requirements

* An **AIO (All-In-One)** server on DBH.

---

## Tutorial

### 1. Installation
Run the following commands in your server terminal to clone the repository and set up the environment:

```bash
git clone [https://github.com/louislam/uptime-kuma.git](https://github.com/louislam/uptime-kuma.git)
cd uptime-kuma
npm run setup

# Install PM2 to keep the process running
npm install pm2 -g && pm2 install pm2-logrotate

# Start the application
pm2 start server/server.js --name uptime-kuma
```