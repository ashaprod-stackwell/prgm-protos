# Stackwell — Program Entry Prototypes

## The decision: Two screens

When a user scans a program QR code, they see a two-screen flow before account creation:

1. **Screen 1, the trust beat.** "You scanned into [program]," partner co-brand, one value line, a security signal. Confirms they are in the right place before anything is asked of them.
2. **Screen 2, the information moment.** What they get (seed, guided milestones, eligibility) and how long it takes, then the fork: create account or sign in.

Why this one: for a first-time investor arriving from a physical scan, separating "am I in the right place?" from "here's the deal" does more than any single-screen version. It earns the tap instead of front-loading a form. This held up across engineering, design, and customer-voice review.

- **Live:** https://ashaprod-stackwell.github.io/prgm-protos/qr-to-sign-up/proto-two-screens.html
- **Source:** [qr-to-sign-up/proto-two-screens.html](./qr-to-sign-up/proto-two-screens.html)

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
