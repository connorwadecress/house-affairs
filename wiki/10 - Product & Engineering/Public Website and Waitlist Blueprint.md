---
created: 2026-07-01
type: product-engineering
status: draft
---

# Public Website and Waitlist Blueprint

This note captures the current planning direction for the first House Affairs public website and owned waitlist. It is not an implementation task and no website code exists yet.

## Source Summary

Connor requested planning for a public-facing House Affairs website that can attract attention, rank well in search, and collect leads before fuller implementation guidance is provided.

The waitlist implementation should be House Affairs-owned development code, use Resend for email delivery, and be based on the provided waitlist/public API blueprint from:

`C:/Users/ConnorCress/source/PersonalDev/Asset-Management/asset-management/docs/waitlist-public-api-blueprint-template.md`

The provided blueprint is a reusable architecture plan. It does not prove the final House Affairs stack, route names, database, environment variables, sender domain, deployment provider, or production configuration.

## Confirmed Facts

- House Affairs is currently in an early foundation stage.
- The repo currently has no production website or application code.
- Connor wants a public brochure-style website.
- Connor wants a waitlist or lead-capture feature.
- Connor wants the waitlist to be House Affairs-owned code, not only a third-party embedded form.
- Connor named Resend as the intended email delivery technology for this feature.
- Connor named Google Search Console, optional PostHog, and Vercel as candidate website/analytics/deployment tools.
- The first website should support public attention, SEO, leads, event discovery, staying in contact, and booking/collaboration interest.

## Assumptions To Validate

- `house-affairs.org` will be the launch domain after domain ownership and DNS access are verified.
- Vercel may be the first hosting provider, but account, team, pricing, and deployment ownership are not verified in this repository.
- The first website may use a framework such as Next.js, but no stack decision has been made.
- The waitlist will require a database or durable storage provider, but no provider has been selected.
- The first public conversion may need more than one intent type, such as event updates, booking House Affairs, collaboration, or working with the collective.

## Open Questions

- Who owns DNS and can point `house-affairs.org` to the deployed site?
- What is the approved launch stack and deployment owner?
- What verified sender domain and email address will Resend use?
- What database or storage provider will hold waitlist submissions?
- What personal data, consent text, unsubscribe path, and retention policy are required before collecting emails?
- Should the first waitlist capture a single email field or also capture intent, name, organization, city, referral source, and marketing consent?
- What official images, videos, logo files, roster details, and social URLs are approved for launch?
- Which analytics tools are approved for the first launch, and what privacy/consent handling is required?

## Website Product Direction

The first website should be a sharp public signal, not an internal system. Its job is to make House Affairs look credible, current, and worth following or booking.

Primary goals:

- Explain House Affairs quickly: Pretoria-rooted modern house music, sessions, events, and community.
- Convert attention into owned audience signal through the waitlist.
- Make the latest sessions easy to watch and share.
- Give venues, collaborators, artists, and listeners a clear way to show interest.
- Establish a search-visible home for House Affairs instead of relying only on social platforms.

Likely first-page sections:

- Hero with strong House Affairs identity, a real session/video/photo asset, and a clear call to action.
- Latest session or featured video.
- Short collective positioning.
- DJ roster or founder/team presence when approved.
- "Next affairs" area for upcoming events, recordings, or "announcements coming soon" only when true.
- Waitlist / stay in contact form.
- Booking or collaboration inquiry path.
- Social links to verified channels only.

Public copy should follow [[05 - Brand & Marketing/Voice and Messaging|Voice and Messaging]] and avoid claims about venues, partnerships, scale, or registration details until evidence is recorded.

## SEO and Discovery Direction

SEO should be designed into the first build instead of added later.

Implementation checklist to validate against current official docs before coding:

- Accurate title, description, canonical URL, and Open Graph metadata.
- `robots.txt` and `sitemap.xml`.
- Fast static or server-rendered pages.
- Descriptive URLs for sessions, DJs, and events if those pages exist.
- Image alt text and accessible headings.
- Structured data only where factually accurate, such as Organization, MusicGroup, Event, or VideoObject if supported by the final content and verified against the current schema documentation.
- Google Search Console property setup after domain access is verified.
- Public launch smoke tests for metadata, crawlability, and social sharing previews.

## Waitlist Product Direction

The waitlist should collect owned demand signal while staying lightweight.

Possible audience intents:

- Stay in contact and hear about future events.
- Get notified about the next House Affairs session or event.
- Book House Affairs or the collective.
- Collaborate, sponsor, host, or work with House Affairs.

The first implementation should avoid collecting unnecessary personal data. Email may be enough for the first version unless Connor decides the conversion funnel needs categories or message fields.

## Waitlist Technical Direction

Adapt the provided blueprint to the actual future website stack instead of copying it directly.

Recommended boundaries:

- Public website UI: renders the brochure site and waitlist form.
- Public waitlist API: anonymous server-side endpoint for lead capture.
- Waitlist feature logic: validation, normalization, duplicate handling, persistence, and response shape.
- Notification boundary: feature-level email service depends on a provider-agnostic notification abstraction.
- Resend infrastructure: Resend is hidden behind server-side notification code and never exposed to the browser.

Likely endpoint shape, subject to stack choice:

```text
POST /api/public/waitlist
```

Minimum request shape, subject to privacy decision:

```json
{
  "email": "person@example.com",
  "deviceId": "<client-generated-browser-id>"
}
```

Minimum stored data concept:

```text
Id
Email
NormalizedEmail
DeviceIdHash
JoinedAtUtc
```

Potential optional fields, only after an explicit privacy/product decision:

```text
Intent
Name
Organization
Message
Source
Referrer
UtmCampaign
Status
ConfirmedAtUtc
IpAddressHash
UserAgentHash
```

Baseline behavior from the blueprint:

- Validate email and device id.
- Normalize email before duplicate checks.
- Hash device id before storage.
- Use database unique constraints for duplicate email and duplicate device checks.
- Persist the waitlist entry before sending email.
- Send welcome/confirmation email through a waitlist email service.
- Log email delivery failure without deleting the saved waitlist entry.
- Keep Resend API keys and sender configuration in server-side environment variables or the hosting secret store.
- Use mock email delivery in local/test environments.
- Verify the sender domain before production email sends.

## Analytics Direction

Analytics should answer product and community questions, not only track vanity traffic.

Questions to answer:

- Which channels send visitors to the website?
- Which sessions or DJs drive signups?
- Which call to action gets the most interaction?
- Are visitors looking for events, bookings, collaboration, or music?
- Which search queries bring people to House Affairs?

Candidate tools named by Connor:

- Google Search Console for search visibility.
- PostHog for product analytics if the team accepts the privacy and implementation trade-offs.
- Vercel platform analytics as a possible hosting-native option if Vercel is selected.

No analytics provider is approved yet. Before launch, record the selected tool, owner, consent/privacy approach, and validation path.

## Phased Implementation Plan

### Phase 0 - Planning Capture

- Save this blueprint in the wiki.
- Record the source blueprint and Connor's request in the evidence trail.
- Keep implementation parked until the next product/design guidance arrives.

### Phase 1 - Pre-Build Verification

- Verify domain ownership and DNS access.
- Confirm official social URLs and account owners.
- Confirm brand assets, public images/video, and launch copy.
- Choose stack, hosting, database, analytics, and deployment owner.
- Define privacy/consent requirements for waitlist data.
- Verify current official docs for Resend, chosen hosting, analytics, and search console setup before coding.

### Phase 2 - Design Direction

- Create a first-viewport design concept around real House Affairs music/media.
- Define the lead capture funnel and form copy.
- Decide if the first site is one page or includes session/event/detail pages.
- Decide what "insanely cool" means in concrete design terms: motion, video, typography, black-and-white identity, live-session energy, Pretoria atmosphere, or another approved direction.

### Phase 3 - Website Build

- Scaffold the website using the approved stack.
- Build the public page and responsive layout.
- Add verified social links and content embeds.
- Add SEO metadata, sitemap, robots, and accessible markup.
- Run local visual and accessibility checks.

### Phase 4 - Waitlist Build

- Add server-side waitlist route.
- Add persistence and unique constraints.
- Add validation and duplicate response handling.
- Add Resend-backed notification service behind a feature-level abstraction.
- Add tests for success, validation, duplicates, email-send failure, and secret-free frontend behavior.

### Phase 5 - Deployment and Launch

- Configure environment variables in the hosting provider.
- Verify sender domain and email configuration.
- Deploy preview and production site.
- Configure exact allowed origins if a separate API host is used.
- Set up Search Console and selected analytics.
- Run smoke tests from the deployed public origin.

## Acceptance Checklist

- No secrets in source control or frontend bundles.
- Public copy uses verified facts only.
- Domain and official social links are verified.
- Waitlist stores only approved data.
- Email address is normalized before uniqueness checks.
- Device id is hashed before storage if used.
- Duplicate submissions are handled at the database level.
- Email sends only after persistence succeeds.
- Resend is server-side only.
- Local/test email delivery is mocked.
- Production email sender domain is verified.
- SEO metadata, sitemap, and crawlability are validated.
- Analytics setup is documented and privacy-reviewed.

## Validation Status

Validated in this documentation pass:

- The referenced blueprint file exists and was read.
- The House Affairs wiki currently identifies no production website or app code.
- The repository currently does not contain an `SOC` directory; planning was saved under the existing product-engineering wiki section.

Not validated yet:

- Domain ownership or DNS access.
- Vercel account/team/project access.
- Resend account, API key, sender domain, or pricing.
- Google Search Console access.
- PostHog account/project access.
- Database/storage provider.
- Final stack or route names.
- Brand assets and launch content approvals.
