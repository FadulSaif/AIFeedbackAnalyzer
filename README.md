AI Feedback Analyzer - Project Documentation
Overview
The AI Feedback Analyzer is an automated n8n workflow that processes daily customer feedback for a bakery business, analyzes it using AI, and generates comprehensive HTML reports. This system transforms raw customer feedback into actionable business intelligence.

Key Features
⏰ Automated Daily Processing
Schedule Trigger: Runs daily at 9:00 AM

Automatic Data Retrieval: Fetches new, unprocessed feedback from Google Sheets

Processing Flag System: Tracks which feedback entries have been analyzed

📊 Intelligent Feedback Analysis
AI-Powered Insights: Uses Google Gemini to analyze customer feedback

Pattern Recognition: Identifies common themes and issues across multiple customers

Sentiment Analysis: Categorizes feedback as positive or negative

📧 Professional Reporting
HTML Email Reports: Generates beautifully formatted daily summaries

Actionable Recommendations: Provides specific improvement suggestions

Executive Summary: Concise overview for quick management review

Technical Architecture
Data Flow Pipeline
1. Data Collection & Trigger
Schedule Trigger: Daily execution at 9:00 AM

Google Sheets Integration: Reads from "Bakery Feedback Responses" spreadsheet

Smart Filtering: Only processes rows where "Processed?" column = "NO"

2. Data Processing
Field Editing: Updates "Processed?" flag from "NO" to "YES" to prevent duplicate processing

Aggregation: Combines all "What could we improve?" feedback into a single dataset

Batch Processing: Handles multiple feedback entries simultaneously

3. AI Analysis Engine
Google Gemini LLM: Advanced natural language processing

Structured Prompting: Specific instructions for bakery context analysis

Temperature Setting: 0.3 for consistent, focused responses

4. Report Generation & Delivery
HTML Formatting: Creates email-friendly report structure

Gmail Integration: Automated email delivery to management

Dynamic Subject Lines: Includes current date in email subject

Report Structure
The AI generates comprehensive HTML reports with these sections:

📊 Daily Feedback Summary
Overview of feedback volume and overall sentiment

High-level insights at a glance

⭐ Average Customer Rating
Summary of rating trends (scale of 1-5)

Daily variations and patterns

Comparative analysis

😊 Positive vs 😞 Negative Ratio
Percentage breakdown of sentiment

Interpretation of what the ratio indicates

Trend analysis

🔍 Top 3 Customer Issues
Ranked list of most frequent concerns

Specific examples from customer feedback

Pattern identification across multiple responses

🚀 Recommended Actions
Immediate (Today)
Quick-win improvements that can be implemented same day

High-impact, low-effort changes

This Week
Strategic improvements requiring planning

Medium-term operational changes

Data Management
Google Sheets Schema
The workflow processes data with these columns:

Timestamp: When feedback was submitted

Customer Name: Optional customer identification

Email: Customer contact information

How would you rate your experience?: 1-5 star rating

What could we improve?: Free-text feedback

Processed?: Workflow tracking flag ("NO"/"YES")

Processing Logic
Incremental Processing: Only analyzes new feedback since last run

State Management: Updates "Processed?" flag to prevent re-analysis

Error Handling: Continues processing even if individual entries fail

AI Prompt Engineering
The system uses a carefully crafted prompt that:

Context Setting
Establishes AI role as "customer experience analyst for a bakery"

Provides clear business context for relevant analysis

Structured Output Requirements
HTML Formatting: Specific section requirements

Actionable Insights: Focus on practical recommendations

Conciseness: Under 500 words total

Pattern Focus: Analysis across multiple customers, not individual complaints

Quality Controls
No Code Blocks: Clean HTML without ```html tags

Email Compatibility: Simple HTML that renders correctly in email clients

Date Stamping: Automatic inclusion of generation date

Use Cases & Benefits
For Bakery Management
Daily Insights: Morning report before business hours

Trend Identification: Spot recurring issues quickly

Data-Driven Decisions: Base improvements on actual customer feedback

Time Savings: Automated analysis代替manual review

Customer Experience Improvement
Rapid Response: Identify and address issues within 24 hours

Proactive Management: Prevent small issues from becoming patterns

Continuous Improvement: Regular feedback incorporation into operations

Setup & Configuration
Prerequisites
Google Sheets with customer feedback form responses

Google Gemini API credentials

Gmail account for report delivery

n8n workflow automation platform

Customization Options
Schedule Timing: Adjust 9:00 AM trigger to suit business needs

Report Recipients: Modify email destination for different stakeholders

Analysis Focus: Update AI prompt for different business contexts

Data Source: Connect to different feedback collection systems

Quality Assurance Features
Consistent Formatting: Standardized report structure daily

AI Temperature Control: Balanced creativity and consistency

Processing Tracking: Prevents data loss or duplicate analysis


