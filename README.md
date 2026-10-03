# Automated Lead Management & CRM Pipeline — v1

An n8n workflow for automating lead collection, scoring, classification, CRM storage, and Telegram notifications.

## Version

v1.0

## Features

- Webhook-based lead collection
- Lead data transformation
- JavaScript-based lead scoring
- Hot / Warm / Cold lead classification
- Conditional workflow branching
- Data Table integration
- Telegram notifications for hot leads
- Webhook response

## Workflow

Webhook
   ↓
Edit Fields
   ↓
JavaScript Lead Scoring
   ↓
IF — Hot Lead?
   ├── TRUE → Data Table → Telegram → Webhook Response
   └── FALSE → Webhook Response

## Lead Scoring

| Criterion | Score |
|---|---:|
| Budget ≥ 50M | +40 |
| Budget ≥ 30M | +25 |
| AI Automation | +20 |
| Website source | +10 |
| Message provided | +10 |

## Lead Classification

| Score | Category |
|---:|---|
| 70+ | Hot |
| 40–69 | Warm |
| Below 40 | Cold |

## Technologies

- n8n
- JavaScript
- Webhooks
- Telegram Bot API
- Data Tables
- Docker

## Project Structure

```text
automated-lead-management-n8n/
│
├── workflows/
│   └── lead-management-v1.json
│
├── screenshots/
│
└── README.md