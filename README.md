# D2C Weekly Sales Intelligence Automation

An AI-powered weekly sales reporting system built with **n8n, Google Sheets, OpenAI, and Gmail**.

This workflow transforms raw D2C sales data into structured business metrics, AI-generated insights, and an automated executive report.

## 🚀 Overview

D2C businesses generate large amounts of sales data, but manually reviewing that data every week can be repetitive and time-consuming.

This automation handles the reporting process automatically:

**Sales Data → Metrics → AI Analysis → Executive Report → Email**

The system helps identify:

- Weekly revenue performance
- Week-over-week revenue changes
- Order volume
- Average order value
- Top-performing products
- Declining products
- Important business risks
- Recommended actions

## 🔄 Workflow

```text
Google Sheets
      ↓
Read Sales Data
      ↓
Calculate Weekly Metrics
      ↓
Build AI Analysis Prompt
      ↓
OpenAI
      ↓
Parse AI Output
      ↓
Build Executive Email
      ↓
Gmail
      ↓
Weekly Sales Intelligence Report
⚙️ Key Features
1. Automated Data Collection

The workflow reads sales records directly from Google Sheets.

Example fields include:

Date
Product
Category
Units Sold
Revenue
Profit
Discount
Sales Channel
Region
2. Weekly Performance Analysis

The workflow calculates:

Current week revenue
Previous week revenue
Revenue change %
Weekly order volume
Average order value
Top-performing products
Product-level week-over-week changes
Declining products

The reporting period is determined dynamically from the available sales data.

3. AI-Powered Business Insights

The calculated metrics are passed to OpenAI for business analysis.

The AI generates:

Executive summary
Top business insight
Biggest warning
Recommended action
Overall weekly sentiment

The AI response is structured so it can be reliably used by the next automation steps.

4. Automated Executive Report

The workflow converts the analysis into a formatted HTML report and sends it automatically through Gmail.

The business owner receives the important information without manually preparing a weekly report.

🧠 Automation Logic

The core principle is:

Calculate first. Interpret second. Deliver automatically.

Instead of sending thousands of raw sales records directly to AI, the workflow first calculates the important business metrics.

AI then interprets the structured metrics and generates business-focused insights.

🛡️ Error Handling

A separate error-handling workflow is included.

If the main workflow encounters an error, an alert can be triggered so the failure does not go unnoticed.

This makes the automation more reliable for real-world use.

🛠️ Technologies Used
Technology	Purpose
n8n	Workflow automation
Google Sheets	Sales data source
OpenAI	AI business analysis
Gmail	Automated report delivery
JavaScript	Data processing and calculations
📊 Example Use Case

A D2C company stores its sales data in Google Sheets.

Every week the automation:

Reads the latest sales data
Calculates weekly metrics
Compares performance with the previous week
Identifies top-performing products
Detects declining products
Sends structured metrics to AI
Generates business insights
Creates an executive report
Sends the report automatically by email
📁 Project Structure
D2C-Weekly-Sales-Intelligence/
│
├── README.md
│
├── workflow/
│   └── D2C-Weekly-Sales-Intelligence.json
│
├── sample-data/
│   └── sales_data.csv
│
├── screenshots/
│   ├── workflow.png
│   ├── sales-data.png
│   ├── ai-insights.png
│   └── email-report.png
│
└── docs/
    └── setup.md
🔮 Future Improvements

Possible extensions include:

Shopify integration
WooCommerce integration
Slack alerts
Meta Ads performance analysis
Google Analytics integration
Inventory monitoring
Customer retention analysis
Automated anomaly detection
Product-level alerts
Dashboard integration
Multi-channel sales reporting
Automated PDF reports
Database integration
💼 What This Project Demonstrates

This project demonstrates practical experience with:

Workflow automation
AI integration
Google Sheets integration
JavaScript data processing
Structured AI outputs
Business reporting
Automated email delivery
Error handling
Data-driven decision support
⚠️ Disclaimer

This is a portfolio/demo project using sample sales data.

The data is illustrative and does not represent a real client.

Business decisions should be validated against actual company data and business context before implementation.

Built with n8n + Google Sheets + OpenAI + Gmail
