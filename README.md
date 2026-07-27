# 🚀 Sales Data Pipeline Automation (n8n)

An end-to-end automated sales data processing pipeline built with n8n. This workflow fetches sales data, splits array items, calculates order totals, filters delivered items, aggregates summary stats by region, and exports a finalized CSV report.

## 🛠️ Tech Stack & Features
- **Automation Engine:** n8n
- **Key Features:**
  - Secure Header Authentication
  - Multi-branching Workflow Design
  - Dynamic Data Transformation & Calculations via Expressions
  - Item Aggregation & Summarization
  - CSV File Generation & Uploading via Binary Stream

## 📊 Workflow Structure
1. **Get & Transform:** Fetches API data -> Splits array -> Calculates totals.
2. **Operations Branch:** Sends raw processed orders to the processing queue.
3. **Analytics Branch:** Filters `delivered` orders -> Summarizes sales by region -> Validates metrics.
4. **Reporting Branch:** Formats metadata -> Generates CSV file -> Uploads final report.

## 🚀 How to Import
1. Download `workflow.json` from this repository.
2. Open your n8n canvas.
3. Press `Ctrl + V` or use **Import from File** to load the complete setup.
