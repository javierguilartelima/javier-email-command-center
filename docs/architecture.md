# System Architecture

## Design objective

Create one modular email management system that can process messages from several accounts without requiring a separate classifier and notification system for each inbox.

The system should reduce inbox-checking time, suppress noise, prevent missed opportunities, and support future expansion without needing a full redesign.

## High-level flow

```text
Email account triggers
        ↓
Normalize message data
        ↓
Deduplicate and validate
        ↓
Fast rule-based filtering
        ↓
Is the classification obvious?
   ├── Yes → Assign category and priority
   └── No  → AI-assisted classification
                    ↓
            Confidence check
                    ↓
      ┌─────────────┴─────────────┐
      ↓                           ↓
High confidence               Low confidence
Execute action                Send to review
      ↓
Apply Gmail labels
      ↓
Notify, summarize, or suppress
      ↓
Log result and relevant metadata
