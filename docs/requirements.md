# Requirements

## Core outcome

The user should spend less time checking inboxes while becoming less likely to miss important messages, deadlines, opportunities, security alerts, or conversations that require action.

## Functional requirements

### Multi-account ingestion

- Connect at least two Gmail accounts in the first version.
- Preserve the source account for every processed email.
- Allow more accounts to be added without redesigning the classifier.

### Classification

Every processed email should receive:

- category;
- priority;
- recommended action;
- confidence;
- short reason for the classification.

### Priority levels

- P0 — Immediate
- P1 — Today
- P2 — This week
- P3 — Review in summary
- P4 — Ignore or archive

### Actions

The system may:

- apply labels;
- notify immediately;
- add to a daily summary;
- register an opportunity;
- create a follow-up reminder;
- archive known low-value messages;
- send uncertain cases to review.

The system must not:

- permanently delete messages;
- automatically send replies;
- expose credentials;
- treat AI classifications as unquestionable.

### Special handling

Verification codes and security alerts should bypass slow AI classification and use direct rules whenever possible.

### Notifications

Immediate notifications should be limited to:

- security events;
- time-sensitive verification messages;
- deadlines;
- interviews;
- job or internship opportunities with high relevance;
- scholarship opportunities;
- direct messages from real people requiring action;
- client or buyer inquiries;
- urgent school communications.

### Review queue

Messages with low classification confidence must be labeled for manual review rather than silently ignored.

## Non-functional requirements

- Modular
- Secure
- Easy to expand
- Cheap to operate
- Clear logs
- Easy to test
- Easy to disable
- No single AI model dependency
- Minimal unnecessary notifications

## Success metrics

Initial metrics:

- important messages detected;
- irrelevant notifications suppressed;
- false positives;
- false negatives;
- opportunities captured;
- emails requiring response;
- estimated inbox-checking time saved.
