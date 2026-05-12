# AI-Powered Gmail Email Classifier for Real Estate

An automated email priority routing system built for residential 
real estate operations using n8n and the Gmail API.

## What It Does

Automatically classifies every incoming email into one of four 
priority tiers in real time:

- 🔴 **CRITICAL** — Wire instructions, closing dates, contract 
termination, executed contracts
- 🟠 **HIGH** — Offers, inspections, appraisals, contingencies
- 🟡 **MEDIUM** — Showings, HOA docs, disclosures, vendor emails
- 🟢 **LOW** — MLS alerts, marketing, brokerage newsletters

Emails matching noise patterns (open house announcements, 
MLS listing alerts, "click to view listing") are automatically 
excluded from labeling entirely.

## How It Works

1. Gmail Trigger fires on every new unread email
2. Full message is fetched via Gmail API
3. Sender, subject, and body are extracted
4. Custom JavaScript classification engine evaluates the email 
   using a first-match-wins priority system
5. Email is routed and labeled in Gmail automatically

## Tech Stack

- n8n (workflow automation)
- Gmail API / Google Workspace
- JavaScript (custom classification logic)

## What I Learned

- How to build rule-based classification engines in JavaScript
- How to connect and authenticate Gmail API in n8n
- How to design workflow routing logic with multiple output branches
- How to translate a real business framework into automated logic
