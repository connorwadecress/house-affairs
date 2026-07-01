---
created: 2026-07-01
type: product-engineering
status: draft
---

# Technical Architecture

## Current Architecture

No production technical architecture exists yet.

Current repository architecture:

- `wiki/` - project brain and operating memory.
- `docs/` - future external-facing docs or exports.
- `src/` - future application/tooling code.

## Current Website / Waitlist Direction

See [[Public Website and Waitlist Blueprint]].

The likely first production surface is a public brochure website with server-side waitlist functionality. The waitlist should be House Affairs-owned code and use Resend behind a server-side notification boundary after the actual website stack is chosen.

Candidate tools named by Connor:

- Vercel for hosting.
- Google Search Console for search visibility.
- PostHog as a possible product analytics option.
- Resend for waitlist email delivery.

These are candidate directions, not verified production configuration.

## Likely Future Needs

- Static or Next.js website for `house-affairs.org`.
- Simple CMS or markdown-driven content archive.
- Analytics reporting.
- Contact/signup collection.
- Venue and partner CRM.
- Event pages and ticketing integrations.

## Defaults To Consider Later

- Use a mainstream framework only when there is a real website or app requirement.
- Keep secrets in hosting/platform environment variables, not in git.
- Prefer platform-native integrations before custom infrastructure.
- If deploying on Vercel later, install the Vercel CLI with `npm i -g vercel` so agents can use `vercel env pull`, `vercel deploy`, and `vercel logs`.
- Keep Resend server-side only; never expose API keys in browser code.
- Add persistence with explicit data retention and privacy handling before collecting public waitlist emails.

## Open Questions

- What hosting platform will be used?
- Is the first website a static page, content archive, or interactive event/community app?
- Who owns deployment credentials?
- What analytics stack should be used?
- What database or storage provider should hold waitlist records?
- What email sender domain and address will be verified for Resend?
