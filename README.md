# 🚀 Automated Sales Data Pipeline (n8n Workflow)

## 📝 Overview
This repository provides a production-ready, highly secure, and optimized n8n workflow designed to streamline sales data processing and report automation. Built using n8n, this ETL pipeline fetches raw order data via API, cleans and enriches items, filters specific fulfillment statuses, computes regional revenue metrics, and automatically posts CSV analytics reports.

---

## ✨ Key Features & Technical Architecture
* **Secure Credential Management:** All sensitive API keys, Assessment IDs (`X-Assessment-ID`), and internal credential tokens are fully sanitized with placeholders (`YOUR_ASSESSMENT_ID`).
* **Automated ETL Data Pipeline:** Fetches nested JSON data, splits order arrays, and calculates individual item totals dynamically (`quantity * unit_price`).
* **Multi-Branching Routing:** Routes data independently into processing queues, filtered delivery analytics (`status == 'delivered'`), and aggregate reporting branches.
* **Regional Analytics & Summarization:** Grouping metrics (Sum, Count, Average) by region and converting results into clean, unified JSON payloads.
* **CSV Report Generation:** Automatically appends generated metadata and converts output into binary CSV files for automated upload.

---

## 🚀 Getting Started

### Prerequisites
* An active **n8n** instance (Cloud or Self-hosted).
* Access to your target API endpoints.

### Installation
1. Download or copy the code from `workflow.json` in this repository.
2. Open your n8n canvas.
3. Press `Ctrl + V` (or select **Import from File / JSON** from the menu) to load the nodes.
4. Replace all placeholders (`YOUR_ASSESSMENT_ID`, `YOUR_CREDENTIAL_ID`) with your active environment headers and credentials.
5. Click **Execute Workflow** to run the pipeline!

---

## 🛠️ Tech Stack
* **Workflow Engine:** n8n Automation
* **Data Interchange:** JSON & CSV
* **Integrations:** REST API, HTTP Webhooks, Header Authentication
* **Logic & Analytics:** Expressions, Multi-branching Workflow, Data Aggregation
