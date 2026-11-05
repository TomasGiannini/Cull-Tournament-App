# Cull — Tournament Fishing Platform (iOS)

> Full-stack tournament management app with AI-powered catch verification. Approved on the Apple App Store.

**Status:** ✅ App Store approved · **Source:** Private — code walkthrough available on request

## What it does

Replaces paper scorecards and disputed catches in fishing tournaments: anglers photograph their catch, AI verifies species and measurement, and live leaderboards update in real time.

## Architecture

- **iOS client:** SwiftUI
- **Backend:** Supabase (PostgreSQL) with 13 Edge Functions (TypeScript/Deno) handling all payment, email, and AI verification logic server-side
- **AI pipeline:** Anthropic API (Claude) for fish detection + measurement validation, routed through admin review queues
- **Payments:** Stripe integration for event registration
- **Geo:** GPS geofencing using Ontario government GIS polygon data to validate fishing zones
- **Notifications:** APNs push

## Engineering highlights

- **AI verification pipeline:** photo → species detection + measurement validation → automated scoring with human-in-the-loop admin review — balances automation with the trust requirements of money-on-the-line tournaments
- **Auto-culling logic:** multi-format leaderboard scoring with XP/rank progression
- **Security:** conducted a structured 8-domain security audit pre-launch; resolved 22 vulnerabilities including 5 critical
- Shipped solo end-to-end: client, backend, payments, AI, app review process

## Media

[Screenshots / App Store link here]

## Why the code is private

Commercial product. Happy to walk through the codebase live in an interview.
