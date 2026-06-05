# Stackwell — Program Entry Prototypes

## The decision: Two screens

**This is the position Product is moving forward with.** When a user scans a program QR code, they see a two-screen flow before account creation:

1. **Screen 1, the trust beat.** "You scanned into [program]," partner co-brand, one value line, a security signal. Confirms they are in the right place before anything is asked of them.
2. **Screen 2, the information moment.** What they get (seed, guided milestones, eligibility) and how long it takes, then the fork: create account or sign in.

Why this one: for a first-time investor arriving from a physical scan, separating "am I in the right place?" from "here's the deal" does more than any single-screen version. It earns the tap instead of front-loading a form. This held up across engineering, design, and customer-voice review.

- **Live:** https://ashaprod-stackwell.github.io/prgm-protos/qr-to-sign-up/proto-two-screens.html
- **Source:** [qr-to-sign-up/proto-two-screens.html](./qr-to-sign-up/proto-two-screens.html)

## For engineering

**Build one templated, config-driven screen, not one per program.** Every program difference is data, not layout. Adding a program should be a config entry plus two image uploads, zero eng.

Program-configurable fields: `program_id`, `program_name`, `partner_name`, `partner_logo`, `hero_image`, `value_prop_line`, `seed_amount`, `benefits[]` (1-4), `eligibility_statement`, `allowed_email_domains[]`, `verification_mode`. Everything else (structure, fork, trust line) stays fixed.

Open decisions to lock before build (these are product rules, not UI states):

- **Null `program_id`** when deep-link attribution fails. Recommend a manual program-code fallback rather than dumping users on the generic login screen.
- **Multi-program enrollment.** Recommend allowing multiple, keyed `(user_id, program_id)`, never overwrite. Makes "nothing starts over" true by construction.
- **Seed double-dip.** Recommend one seed per user at launch until fraud monitoring exists. Fund-flow decision, loop in Sam.
- **Eligibility posture.** Recommend soft-warn on non-matching email domains, configurable per program.

Instrument the current flow now so there is a real baseline: QR landing viewed, fork tapped, account created, application started, all tagged with `program_id`.

---

## Background: how we got here

### Scenario

A user scans a QR code and lands inside Stackwell for a program they're likely seeing for the first time. These prototypes drop the assumption that the user already knows the program name, who's behind it, or what they're signing up for.

### The question

How much context does a user need to be sure they are in the right place + ready to commit to creating an account?

**Range of orientations the QR entry point flow has to handle:**

- Direct from a partner / Stackwell email
- Forwarded link / QR from a friend or colleague
- Campus scan / public scan
- Through a Stackwell ambassador

### The axis we examined

Four positions on the context axis (V1 prototypes):

1. **Name only** — program name + one line → sign up / log in
2. **Full context** — everything → sign up / log in
3. **Scroll gate** — everything → sign up / log in
4. **Two screens** — waterfall approach: trust beat → info → sign up / log in (the position chosen above)

Two visual treatments side by side to weigh emotional payload (image hero) against simplicity and reusability (light gradient).

#### Image hero
- **Live:** https://ashaprod-stackwell.github.io/prgm-protos/qr-to-sign-up/proto-axis-interactive.html
- **Source:** [qr-to-sign-up/proto-axis-interactive.html](./qr-to-sign-up/proto-axis-interactive.html)

#### Light gradient hand-off
- **Live:** https://ashaprod-stackwell.github.io/prgm-protos/qr-to-sign-up/proto-axis-interactive-gradient.html
- **Source:** [qr-to-sign-up/proto-axis-interactive-gradient.html](./qr-to-sign-up/proto-axis-interactive-gradient.html)
