# job-aggregator-n8n
# Indian Tech Job Aggregator & Daily Digest (n8n Workflow)

## 📌 Overview
This project automates the process of finding and sharing the latest **tech job postings in India**.  
It uses **n8n workflow automation** to fetch jobs from the **Adzuna Jobs API**, store them in Google Sheets, and send a **daily job digest** via Gmail and Slack.  

This workflow was created to save time in manual job searching and also to generate content for a **YouTube channel** that shares daily job updates.

---

## ⚡ Features
- Fetches up to **50 latest tech jobs** from Adzuna API daily
- Extracts job details:
  - Job Title
  - Company
  - Location
  - Category
  - Posted Date
  - Salary Range
  - Application URL
- Stores all results in **Google Sheets** for tracking
- Sends **Top 10–15 jobs** to Gmail and Slack as a formatted digest
- Can be scheduled to run daily via Cron

---

## 🛠️ Tech Stack
- **n8n** (workflow automation)
- **Adzuna Jobs API** (job listings)
- **Google Sheets API** (data storage)
- **Gmail API** (daily digest via email)
- **Slack API** (team notifications)

---

## 📂 Workflow Steps
1. **Cron Node** → Triggers workflow daily at 9 AM  
2. **HTTP Request Node** → Fetches job listings from Adzuna API  
3. **Function Node** → Formats and cleans job data  
4. **Google Sheets Node** → Stores all jobs in a sheet  
5. **Function Node (Top 15)** → Selects the top jobs for notification  
6. **Gmail Node** → Sends daily digest email  
7. **Slack Node** → Posts digest in a Slack channel  

---

## 🚀 Setup Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/job-aggregator-n8n.git
