---
created: 2026-07-01
type: product-engineering
status: draft
---

# Data Model

This is a conceptual data model for future tooling. It is not a database schema.

## Core Entities

- Session.
- DJ.
- Location.
- Venue.
- Event.
- Partner.
- Content asset.
- Platform post.
- Audience metric snapshot.
- Waitlist lead.
- Correspondence item.
- Decision.
- Open question.

## Minimum Fields To Track Manually First

### Session

- Date.
- Title.
- DJ(s).
- Location.
- Status.
- YouTube link.
- Instagram link(s).
- Production notes.
- Analytics snapshot.
- Public feedback snapshot.

### Venue

- Name.
- Location.
- Contact.
- Fit notes.
- Pipeline stage.
- Last correspondence.
- Constraints.

### Event

- Date.
- Venue.
- Goal.
- Lineup.
- Capacity.
- Budget.
- Ticketing/RSVP.
- Compliance status.
- Outcome.

### Public Feedback Item

- Source platform.
- Source URL.
- Video/session.
- Public author handle.
- Comment ID when available.
- Date captured.
- Feedback type.
- Sentiment.
- Actionability.
- Summary.
- Owner/status if it creates a task.

### Waitlist Lead

- Email.
- Normalized email.
- Joined timestamp.
- Lead intent, if approved.
- Source/referrer/UTM fields, if approved.
- Consent status, if required.
- Status, such as active, unsubscribed, duplicate, or imported, if required.
- Device hash, IP hash, or user agent hash only if the team approves the privacy and abuse-prevention trade-off.

## Rule

Do not convert this into a production schema until there is a clear app/tooling requirement.
