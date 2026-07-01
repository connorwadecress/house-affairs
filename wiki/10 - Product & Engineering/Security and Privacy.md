---
created: 2026-07-01
type: product-engineering
status: draft
---

# Security and Privacy

## Rules

- Do not commit credentials, passwords, API keys, recovery codes, private phone numbers, or private emails.
- Do not store raw customer or attendee personal data unless there is a clear need and handling policy.
- Do not record secret values in wiki notes.
- For accounts, record the role owner and system name, not the secret itself.
- For public events, define consent handling before filming attendees.

## Current Unknowns

- Who controls Instagram access.
- Who controls YouTube access.
- Who controls the domain registrar.
- What storage is used for raw footage.
- What personal data will be collected for events or signups.
- What personal data the public website waitlist should collect.
- What privacy notice, consent wording, retention policy, and unsubscribe process are required before launching waitlist collection.
- Which team member owns Resend, analytics, and hosting access.

## Waitlist Rules To Carry Forward

- Collect the minimum data needed for the first public use case.
- Do not expose Resend API keys or database credentials in frontend code.
- Hash browser/device identifiers before storage if they are used for duplicate prevention.
- Treat email addresses and lead messages as personal data.
- Do not store IP address, user agent, referral, or UTM data unless the team makes an explicit privacy and retention decision.
- Use mock email delivery in local/test environments.
- Verify production sender domain and sender address before real email sends.

## Future Checklist

- Password manager ownership.
- Platform access roles.
- Recovery processes.
- Two-factor authentication.
- Backup policy.
- Data retention policy.
- Consent/release workflow for filmed attendees.
- Waitlist privacy notice and unsubscribe path.
- Analytics consent/privacy decision.
