
# 📬 email-lead-collector

Extract emails from any public website and save them directly into a CSV file — fully automated using n8n.

🔧 This project is beginner-friendly, useful for freelancers, marketers, and small business owners who want to collect leads without coding.

---

## 🌟 Features / คุณสมบัติเด่น

- 🌐 Input any website URL (e.g., https://example.com)
- 🕷️ Scrape all visible emails from the HTML
- 📤 Export results to a clean `.csv` file
- 🧩 100% native nodes (no community node required)
- 🔐 Safe headers (User-Agent spoofing)
- 🐞 Prevents common n8n errors: undefined split, bad response body, binary write error

---

## 📸 Demo (GIF)

![demo](./demo/email-lead-collector-demo.gif)

---

## 🚀 How to Use / วิธีใช้งาน

1. 🧱 **Manual Trigger** → Run flow manually or schedule it
2. 🔧 **Set Node** → Input a list of target URLs
```json
{
  "websiteList": "https://example.com, https://anotherdomain.com"
}
```
3. 🧠 **Function Node** → Split and clean the list
4. 🌍 **HTTP Request Node** → Fetch each web page (Response Format: `String`)
5. 🔍 **Regex Match Node** → Extract valid emails
6. 📝 **Write Binary File Node** → Save results as `emails.csv`

---

## 📥 Output File / ผลลัพธ์

- File: `emails.csv`
- Format:
```csv
email,source
john@example.com,https://example.com
info@anotherdomain.com,https://anotherdomain.com
```

---

## 📦 What’s Included / ใน ZIP นี้มี

- `email-lead-collector.json` → n8n Flow
- `README.md` → This file
- `demo/email-lead-collector-demo.gif` → Preview
- Optional CSV sample

---

## 📌 Note / หมายเหตุ

- This flow is designed to work on n8n `v1.94+`, no community node required
- Tested in both Docker and desktop version

---

## 🧠 Who is this for? / เหมาะกับใคร?

- Marketers doing outreach
- Freelancers generating leads
- Devs testing scraping workflow
- Anyone building email lists (legally and responsibly)

---

## 🛠️ Dev Info

- Author: Nuntin Padmadin
- GitHub: [github.com/Nuntin/n8n-devops-bots](https://github.com/Nuntin/n8n-devops-bots)

---
