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

## Rule

Do not convert this into a production schema until there is a clear app/tooling requirement.
