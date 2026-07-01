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

## Open Questions

- What hosting platform will be used?
- Is the first website a static page, content archive, or interactive event/community app?
- Who owns deployment credentials?
- What analytics stack should be used?
