---
created: 2026-07-01
type: open-questions
status: active
---

# Open Questions

Use this note for unknowns that affect decisions. Do not guess these in strategy, public copy, contracts, or operations.

## OQ-001 - What are the official business registration details?

- **Owner:** Connor / founding team.
- **Opened:** 2026-07-01
- **Why it matters:** Legal name, registration number, director/member details, banking, invoices, contracts, venue agreements, and compliance.
- **Current best answer:** Founder statement says House Affairs is a registered business.
- **Evidence needed:** Registration certificate or official registry record.
- **Affected notes:** [[08 - Finance & Legal/Legal and Compliance|Legal and Compliance]], [[02 - Business Model/Registered Business|Registered Business]]
- **Status:** Open

## OQ-002 - Who owns and administers `house-affairs.org`?

- **Owner:** Connor.
- **Opened:** 2026-07-01
- **Why it matters:** Website, email, DNS, brand protection, deployment, and platform integrations.
- **Current best answer:** Founder statement says the domain is owned.
- **Evidence needed:** Registrar screenshot/export, DNS access owner, renewal date, nameservers.
- **Affected notes:** [[10 - Product & Engineering/Website Plan|Website Plan]]
- **Status:** Open

## OQ-003 - What are the official public handles and access owners?

- **Owner:** Connor.
- **Opened:** 2026-07-01
- **Why it matters:** Brand consistency, platform operations, analytics, security, and delegation.
- **Current best answer:** Screenshot shows Instagram handle `houseaffairs.wav`; public YouTube extraction confirmed `https://www.youtube.com/@house.affairs` and channel ID `UCG7qrr_JjGbb8rN_tl38Zdg`.
- **Evidence needed:** Direct platform access confirmation, official URL list, and YouTube Studio/Instagram account owner confirmation.
- **Affected notes:** [[04 - Content & Media/Instagram Account|Instagram Account]], [[04 - Content & Media/YouTube Channel|YouTube Channel]]
- **Status:** Open

## OQ-004 - What is the formal decision authority across the four-person team?

- **Owner:** Founding team.
- **Opened:** 2026-07-01
- **Why it matters:** Prevents accidental commitments around venues, money, brand, events, or ownership.
- **Current best answer:** Draft authority exists in [[Working Agreement]].
- **Evidence needed:** Team confirmation or meeting record.
- **Affected notes:** [[Working Agreement]], [[Tension Log]]
- **Status:** Open

## OQ-005 - What venue names and locations are exact?

- **Owner:** Venue research owner, TBD.
- **Opened:** 2026-07-01
- **Why it matters:** Outreach, partnership research, public mentions, and event planning.
- **Current best answer:** First desktop research verified several details: Moka Social Club is at 378 Milner St, Waterkloof, Pretoria; Billy Boys & Co is at Forest Walk, 27 Maroelana St, Hazelwood, Pretoria based on its official public site bundle; Lucky Rodrigo Restaurant & Bar is at c/o The Hillside Street and Alpine Way, Lynnwood, Pretoria. Connor later reported seeing Moka Instagram stories with running-event afterpoints and live DJs, plus regular daytime live DJs. These are venue identity/location facts plus founder/operator observations, not partnership or event-availability facts.
- **Evidence needed:** Direct venue confirmation of contact owners, existing DJ/event policies, filming permission, sound constraints, costs, and availability. For Moka specifically, save screenshots/highlights/posts or direct confirmation of running-event/live-DJ activity.
- **Affected notes:** [[06 - Events & Venues/Venue Pipeline|Venue Pipeline]]
- **Status:** Partially answered; still open for event-specific details.

## OQ-006 - What music licensing and event compliance requirements apply?

- **Owner:** Legal/compliance owner, TBD.
- **Opened:** 2026-07-01
- **Why it matters:** Public DJ sets, YouTube uploads, monetization, ticketed events, venue agreements, and livestreams may create rights obligations.
- **Current best answer:** Unknown.
- **Evidence needed:** Legal research from official South African sources and platform policies; professional advice if commitments become material.
- **Affected notes:** [[08 - Finance & Legal/Legal and Compliance|Legal and Compliance]], [[04 - Content & Media/Weekly DJ Sets Workflow|Weekly DJ Sets Workflow]]
- **Status:** Open

## OQ-007 - What is the approved first website stack, host, and deployment owner?

- **Owner:** Connor / technical owner TBD.
- **Opened:** 2026-07-01
- **Why it matters:** The waitlist architecture, deployment flow, environment variables, analytics setup, and cost profile depend on the stack and hosting provider.
- **Current best answer:** Connor named Vercel as a candidate free hosting path and mentioned co-founder/collaborator access, but no account, team, project, pricing, or deployment access evidence is recorded.
- **Evidence needed:** Chosen stack, hosting account/team, deployment owner, domain/DNS access, and current official provider docs/pricing if cost assumptions matter.
- **Affected notes:** [[10 - Product & Engineering/Website Plan|Website Plan]], [[10 - Product & Engineering/Technical Architecture|Technical Architecture]], [[10 - Product & Engineering/Public Website and Waitlist Blueprint|Public Website and Waitlist Blueprint]]
- **Status:** Open

## OQ-008 - What privacy and consent standard applies to the public waitlist?

- **Owner:** Connor / legal-compliance owner TBD.
- **Opened:** 2026-07-01
- **Why it matters:** The public waitlist will collect personal data and may send email. Data fields, consent text, unsubscribe handling, storage, retention, and analytics must be decided before launch.
- **Current best answer:** Unknown. Connor wants a waitlist and named Resend for email delivery, but privacy wording and data retention are not defined.
- **Evidence needed:** Approved privacy/consent copy, data fields, retention policy, unsubscribe path, and compliance review appropriate to the launch context.
- **Affected notes:** [[10 - Product & Engineering/Security and Privacy|Security and Privacy]], [[10 - Product & Engineering/Public Website and Waitlist Blueprint|Public Website and Waitlist Blueprint]]
- **Status:** Open

## OQ-009 - What lead intent should the waitlist capture?

- **Owner:** Connor / founding team.
- **Opened:** 2026-07-01
- **Why it matters:** A single email waitlist is simpler, but House Affairs may need to distinguish event updates, booking inquiries, collaboration, sponsorship, venue interest, and people who want to work with the collective.
- **Current best answer:** Connor suggested stay in contact, see next events, work with House Affairs, or book House Affairs collective as possible waitlist ideas.
- **Evidence needed:** Founder/team decision on first-form fields and routing.
- **Affected notes:** [[10 - Product & Engineering/Website Plan|Website Plan]], [[10 - Product & Engineering/Public Website and Waitlist Blueprint|Public Website and Waitlist Blueprint]], [[03 - Audience & Community/Community Strategy|Community Strategy]]
- **Status:** Open

## OQ-010 - What database or storage provider will hold waitlist records?

- **Owner:** Technical owner TBD.
- **Opened:** 2026-07-01
- **Why it matters:** Duplicate handling, migrations, backups, privacy controls, and deployment configuration depend on storage choice.
- **Current best answer:** Unknown. The provided blueprint requires durable persistence but does not choose a House Affairs provider.
- **Evidence needed:** Selected provider, schema/migration approach, access owner, backup/retention plan, and test strategy.
- **Affected notes:** [[10 - Product & Engineering/Data Model|Data Model]], [[10 - Product & Engineering/Public Website and Waitlist Blueprint|Public Website and Waitlist Blueprint]]
- **Status:** Open

## OQ-011 - What verified assets and public copy are approved for the first website?

- **Owner:** Connor / brand owner TBD.
- **Opened:** 2026-07-01
- **Why it matters:** A public site should not publish unapproved roster details, venue/event claims, brand assets, or partnership language.
- **Current best answer:** Existing wiki notes contain draft positioning and public platform-derived copy, but final website copy/assets are not approved.
- **Evidence needed:** Approved logo files, imagery/video, roster names, social links, launch copy, and any event/session claims.
- **Affected notes:** [[05 - Brand & Marketing/Brand Foundations|Brand Foundations]], [[05 - Brand & Marketing/Voice and Messaging|Voice and Messaging]], [[10 - Product & Engineering/Website Plan|Website Plan]]
- **Status:** Open

## OQ-012 - Which analytics tools and consent approach should the first website use?

- **Owner:** Connor / technical owner TBD.
- **Opened:** 2026-07-01
- **Why it matters:** Search and product analytics affect privacy, scripts, consent, performance, and reporting.
- **Current best answer:** Connor mentioned Google Search Console and optional PostHog; no final analytics decision or account access is recorded.
- **Evidence needed:** Selected analytics tools, account/project owners, privacy/consent decision, and launch validation steps.
- **Affected notes:** [[10 - Product & Engineering/Website Plan|Website Plan]], [[10 - Product & Engineering/Public Website and Waitlist Blueprint|Public Website and Waitlist Blueprint]]
- **Status:** Open

## OQ-013 - Is House 22 currently operating and contactable?

- **Owner:** Venue research owner, TBD.
- **Opened:** 2026-07-01
- **Why it matters:** Public historical sources position House 22 as important to Pretoria deep-house history, but current operating status affects whether it belongs in the active venue pipeline or only the reference map.
- **Current best answer:** Unknown. First research found historical/directory evidence, but no current official operating confirmation.
- **Evidence needed:** Current official website/social account, current booking contact, current address, recent events, and direct confirmation from the venue or credible operator.
- **Affected notes:** [[06 - Events & Venues/House 22|House 22]], [[06 - Events & Venues/Venue Pipeline|Venue Pipeline]], [[09 - Research & Intelligence/Pretoria House Music Market|Pretoria House Music Market]]
- **Status:** Open

## OQ-014 - Which compliance responsibilities sit with House Affairs versus the venue for a first DJ night?

- **Owner:** Legal/compliance owner, TBD.
- **Opened:** 2026-07-01
- **Why it matters:** SAMRO, SAMPRA, City of Tshwane, YouTube, venue contracts, filming consent, and ticketing terms can attach to different parties depending on whether House Affairs is a DJ, promoter, venue hirer, content publisher, or event owner.
- **Current best answer:** Unknown. Official sources confirm licensing/compliance issues exist, but not the exact responsibility split for House Affairs' first event structure.
- **Evidence needed:** Event format decision, venue licence confirmation, SAMRO/SAMPRA guidance for the specific setup, Tshwane applicability, written venue terms, filming consent plan, and professional advice if commitments become material.
- **Affected notes:** [[08 - Finance & Legal/Legal and Compliance|Legal and Compliance]], [[06 - Events & Venues/Event Strategy|Event Strategy]], [[06 - Events & Venues/Venue Pipeline|Venue Pipeline]]
- **Status:** Open

## OQ-015 - Which first venue outreach format is approved?

- **Owner:** Connor / founding team.
- **Opened:** 2026-07-01
- **Why it matters:** Outreach wording and target venue choice depend on whether House Affairs is asking for a filmed session, a low-risk DJ slot, a recurring night, or a ticketed event.
- **Current best answer:** Research recommends a filmed-session ask for Moka Social Club and a low-risk venue-hosted DJ-slot ask for Lucky Rodrigo or Billy Boys. Connor's later observation of Moka live-DJ activity strengthens Moka as the first filmed-session target, but the exact ask has not been approved by the founding team.
- **Evidence needed:** Founder/team decision on first outreach objective, owner, proof links, date window, and what House Affairs is prepared to provide.
- **Affected notes:** [[06 - Events & Venues/Moka Social Club|Moka Social Club]], [[06 - Events & Venues/Lucky Rodrigo|Lucky Rodrigo]], [[06 - Events & Venues/Billy Boys & Co|Billy Boys & Co]], [[06 - Events & Venues/Partnership Outreach|Partnership Outreach]]
- **Status:** Open
