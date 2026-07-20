# Javier Email Command Center

A multi-account email triage and opportunity management system built with n8n, Gmail, rules, and AI-assisted classification.

## Project status

Early development.

## Problem

Important emails are spread across multiple accounts and mixed with promotions, newsletters, spam, social notifications, verification messages, school communications, job opportunities, internships, scholarships, and potential client inquiries.

Manually checking every inbox wastes time and still creates the risk of discovering important messages too late.

## Goal

Build one long-term system that:

- monitors multiple email accounts;
- identifies important and actionable messages;
- suppresses low-value noise;
- classifies messages by category and priority;
- applies labels to the original inbox;
- sends immediate alerts only when necessary;
- creates summaries for non-urgent messages;
- tracks opportunities and follow-ups;
- avoids deleting messages automatically;
- remains modular, secure, and maintainable.

## Initial scope

The first usable version will include:

1. Two connected email accounts.
2. Rule-based filtering for obvious messages.
3. AI classification only for ambiguous messages.
4. Gmail labels for categories and priorities.
5. Immediate notification for urgent messages.
6. A review queue for uncertain classifications.
7. Basic logging and error handling.

## Planned categories

- Urgent and actionable
- Opportunity
- Real person or conversation
- Account and security
- School and administration
- Useful but not urgent
- Promotion or newsletter
- Spam or irrelevant
- Needs review

## Safety principles

- No automatic deletion.
- No credentials or personal emails stored in GitHub.
- Sensitive information will be anonymized in screenshots and examples.
- Destructive actions require explicit review.
- Rules will be used before AI whenever possible.

## Technology

- n8n
- Gmail
- Google Sheets
- Telegram or another notification channel
- Rule-based filtering
- AI-assisted classification
- GitHub for documentation and version control

## Repository structure

```text
docs/          Project requirements, architecture, decisions, and tests
workflows/     Sanitized n8n workflow exports
examples/      Anonymized sample inputs and outputs
screenshots/   Clean portfolio screenshots
diagrams/      Architecture and workflow diagrams
