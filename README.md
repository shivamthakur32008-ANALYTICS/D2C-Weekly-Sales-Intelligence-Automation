# D2C Weekly Sales Intelligence Automation

An AI-powered weekly sales intelligence system for D2C/e-commerce businesses.

This automation takes raw sales data from Google Sheets, calculates weekly business metrics, uses AI to generate actionable insights, and automatically delivers an executive sales report by email.

The goal is simple:

**Raw sales data → Business metrics → AI analysis → Executive report → Automated delivery**

---

## 🚀 What This Automation Does

Every week, the workflow automatically:

1. Reads sales data from Google Sheets
2. Calculates weekly revenue and order metrics
3. Compares the current week with the previous week
4. Identifies top-performing products
5. Detects products with declining performance
6. Sends the calculated metrics to an AI model
7. Generates structured business insights
8. Builds a professional HTML email report
9. Sends the report through Gmail
10. Sends an alert through Slack
11. Logs the report execution
12. Uses a separate error-handling workflow for failures

No manual weekly reporting is required.

---

## 🧩 Workflow Architecture

```text
Weekly Trigger
      ↓
Google Sheets
(Read Sales Data)
      ↓
Calculate Metrics
      ↓
Build AI Prompt
      ↓
OpenAI
(Generate Insights)
      ↓
Parse AI Output
      ↓
Build HTML Report
      ↓
Gmail
      ↓
Slack Alert
      ↓
Report Log

A separate error-handling workflow is included to notify when the main workflow encounters an error.

📊 Business Metrics

The workflow is designed to analyze metrics such as:

Weekly revenue
Previous-week revenue
Revenue growth/decline %
Weekly orders
Average order value
Top-performing products
Product-level week-over-week performance
Declining products
Revenue trends
Business risks
Recommended actions

The calculations are performed before the AI analysis so that the AI works from structured business data rather than raw spreadsheet rows.

🤖 AI-Powered Analysis

The AI layer converts the calculated metrics into structured business insights.

The generated output includes:

Executive summary
Top insight
Warning
Recommended action
Weekly sentiment

The AI is used for interpretation and business reasoning, while numerical calculations are handled separately in the workflow.

This separation helps reduce the risk of the AI inventing or incorrectly calculating business metrics.

📧 Automated Executive Report

The workflow generates a formatted HTML sales report and sends it automatically through Gmail.

The report is designed to give a business owner a quick view of:

What happened → Why it matters → What should be investigated next

🛡️ Error Handling

The project also includes a separate error-handling workflow.

If the main workflow fails, an alert can be triggered so that the failure does not go unnoticed.

This is important for production-style automation because a workflow that silently fails is not reliable enough for business use.

🗂️ Project Files
Workflow

D2C Weekly Sales Intelligence Report.json

Main n8n workflow containing the complete automation.

Error Handler

D2C Sales Report - Error Handler.json

Separate workflow for handling workflow failures.

Screenshots
Workflow.png — Complete workflow architecture
Calculate_metrics.png — Calculated business metrics
AI insights.png — AI-generated analysis
Gmail.png — Automated email report
Error handler.png — Error-handling workflow
Report log.png — Report execution logging
Dummy_data.png — Example sales dataset
Demo

A recorded walkthrough demonstrating how the automation works.

🛠️ Technology Stack
n8n — Workflow automation
Google Sheets — Sales data source
JavaScript — Business metric calculations and data processing
OpenAI — AI-generated business insights
Gmail — Automated report delivery
Slack / Webhooks — Notifications
HTML/CSS — Executive report formatting
🔄 Example Use Case

Imagine a D2C brand has hundreds or thousands of sales records in Google Sheets.

Instead of manually opening the spreadsheet every Monday and asking:

How much did we sell?
Did revenue increase or decrease?
Which products performed best?
Which products are declining?
What should we investigate?
What action should the business take?

The automation performs the reporting process automatically.

The business owner receives a structured weekly report without manually calculating the numbers.

📈 Why This Matters

The value of this system is not simply sending an email.

The workflow creates a repeatable reporting process:

Data → Analysis → Insight → Action

This can help reduce repetitive reporting work and give decision-makers a faster view of business performance.

🔐 Security

This repository contains demonstration data and workflow configuration only.

Before deploying the workflow:

Add your own Google Sheets credentials
Add your own OpenAI credentials
Add your own Gmail credentials
Configure Slack/webhook credentials
Never commit API keys, passwords, tokens, or private business data

Credentials should always be stored inside n8n's credential system rather than hard-coded into workflow files.

⚙️ How To Use
1. Import the workflow

Import:

D2C Weekly Sales Intelligence Report.json

into your n8n instance.

2. Configure credentials

Connect:

Google Sheets
OpenAI
Gmail
Slack/webhook
3. Connect your sales data

Use a Google Sheet containing your sales records.

Example structure:

date
product_name
category
units_sold
revenue
profit
discount_percent
sales_channel
region
4. Configure report recipients

Set the required email address and notification destination.

5. Test the workflow

Run the workflow manually first and verify:

Calculated metrics
AI output
Email formatting
Notifications
Report logging
6. Activate the schedule

Once testing is complete, activate the weekly trigger.

🎥 Demo

Watch the complete workflow demonstration:

▶ Watch the Automation Demo - https://www.loom.com/share/4446427ce3c243549227fc69266ee5ff

🧠 Key Design Principle

The workflow separates deterministic calculations from AI interpretation.

Raw Data
   ↓
JavaScript Calculations
   ↓
Verified Metrics
   ↓
AI Interpretation
   ↓
Business Report

This is intentional.

AI should help interpret business information, while important numerical calculations should be handled deterministically whenever possible.

🚧 Current Scope

This project is a demonstration/prototype of a D2C weekly sales intelligence system.

For production deployment, additional features could include:

Database storage
Historical trend analysis
Multiple sales channels
Shopify integration
Automated anomaly detection
Inventory analysis
Customer cohort analysis
Customer acquisition metrics
Profitability analysis
Dashboard integration
Automated recommendations
Monitoring and retry logic
🔮 Future Improvements

Potential next versions could integrate:

Shopify → Google Sheets/Database → n8n → AI → Email/Slack → Dashboard

This would allow the system to move from a spreadsheet-based reporting workflow toward a more complete e-commerce intelligence platform.

👤 Author

Built by Shivam Thakur

Focused on building practical automation systems combining:

AI
Business analytics
Financial analysis
Workflow automation
Data-driven decision making
⭐ Project Objective

This project demonstrates how repetitive business reporting can be transformed into an automated intelligence workflow.

The broader objective is to build automation systems that do more than move data between applications:

They should help businesses understand their data and make better decisions.


---

# 2. GitHub Topics / Tags

Your current tags are okay, but I would change them to these:

### Use these 10:

```text
n8n
ai-automation
workflow-automation
business-automation
sales-automation
sales-analytics
d2c
ecommerce
google-sheets
openai
If GitHub allows more, add:
business-intelligence
data-analysis
javascript
gmail-automation
reporting-automation
Best 5 if you want to keep it tight
n8n
ai-automation
business-automation
sales-analytics
d2c
One important change to your current repo

Your screenshot shows the files are all sitting in the root directory:

AI insights.png
Calculate_metrics.png
D2C Sales Report - Error Handler.json
D2C Weekly Sales Intelligence Report.json
Dummy_data.png
Error handler.png
Gmail.png
README.md
Report log.png
Workflow.png

That's acceptable for a small portfolio project, but don't waste time reorganizing it now.

Your bigger priority is:
