# BIGWINZ BET — Brand Identity & Freebuff Implementation Brief

**Product:** BIGWINZ BET  
**Repository:** ntamauwe-cmyk/bigwinz  
**Target branch:** main  
**Purpose:** Authoritative brand direction and implementation brief for the existing BIGWINZ product. This document records a proposed premium visual system; it is not a claim that final logo artwork or production UI assets have already been created.

## Brand direction

Create an original, premium, confident sportsbook experience with a clear visual identity, fast information scanning, and polished interaction states. BIGWINZ should feel credible and energetic without looking childish, excessively neon, crypto-themed, or like a reskin of another betting product. Do not copy competitors' layouts, logos, illustrations, or proprietary visual assets.

## Core palette

- Deep graphite: `#080A0F`
- Primary surface: `#0D1017`
- Raised surface: `#121722`
- Elevated surface: `#171C26`
- Hover / selected surface: `#1D2330`
- Electric lime accent: `#B7F23A`
- Alternate lime accent: `#A8E82F`
- Electric blue secondary accent: `#3D8BFF`
- Primary text: `#F5F7FA`
- Secondary text: `#A7B0BE`
- Muted text: `#737E8E`
- Borders / dividers: `#293140`

Use lime sparingly for key actions, positive emphasis, selected states, and important odds-related accents. Use blue for secondary emphasis and informational states. Maintain readable contrast and avoid using accent colors as large, distracting backgrounds.

## Logo and brand assets

Develop a distinctive BIGWINZ wordmark and a simple forward-motion-inspired symbol that can work at small sizes, in app navigation, and as a favicon. The mark must be original and must not imitate an existing sportsbook or third-party identity. Keep logo construction, spacing, light/dark variants, and minimum-size guidance consistent. Treat any generated mark as a concept pending approval; do not claim trademark clearance or that final approved vector artwork exists unless it has actually been supplied and approved.

## Product-wide application

Apply a coherent design system across all existing relevant pages and states, including:
- Home and sports discovery
- Sport, league, fixture, and event views
- Live events and live score states
- Odds selection and bet slip
- My bets, bet history, and transaction details
- Wallet, deposits, withdrawals, and payment status
- Promotions and offers
- Sign-in, registration, password recovery, and verification
- Profile, preferences, responsible-gambling and security settings
- Admin and operational interfaces, where present

Preserve each page's purpose and existing information hierarchy. Build reusable tokens and components for typography, spacing, buttons, inputs, cards, tabs, navigation, status indicators, modals, notifications, and loading/empty/error states. Keep mobile, tablet, and desktop layouts intentional and responsive.

## UX and accessibility

Prioritize clear odds and event information, legible typography, predictable navigation, visible focus states, adequate touch targets, keyboard usability, and accessible contrast. Use restrained motion with reduced-motion support. Provide polished loading, empty, success, pending, unavailable, and error states. Avoid visual clutter and misleading urgency.

## Implementation constraints — do not rebuild

Freebuff must first inspect the existing repository and report its framework, routes, components, styling approach, integrations, and current implementation. Then implement this brand direction in the existing codebase with the smallest safe changes.

- Do not rebuild the application or replace its architecture.
- Do not delete, reset, restore, or overwrite existing working features.
- Preserve existing routes, authentication, data models, APIs, backend logic, payment integrations, bet placement, odds handling, settlement, and admin permissions.
- Do not invent live odds, successful deposits, withdrawals, bets, payouts, or settlements. Retain real integration responses and accurately represent unavailable or sandbox functionality.
- Do not introduce unrelated products, shared credentials, or cross-project integrations.
- Do not hardcode secrets or expose environment variables.
- Reuse existing dependencies and components where practical; justify any new dependency.
- Do not claim regulatory approval, certification, or production readiness without evidence.

## Suggested execution sequence

1. Audit the current repository and identify the safest UI-only implementation plan.
2. Establish design tokens and shared components.
3. Apply the system consistently to the existing pages, without removing functionality.
4. Verify responsive behavior, accessibility basics, and all existing user flows.
5. Run the project's available type checks, linting, tests, and build; fix regressions introduced by the changes.
6. Report files changed, checks run and their actual results, known limitations, and any work requiring live credentials or operational verification.

## Acceptance criteria

- BIGWINZ has a consistent, original premium identity across the existing product.
- Existing application behavior and integrations remain intact.
- No fake betting, payment, or settlement outcomes are introduced.
- Main user journeys remain navigable and usable on mobile and desktop.
- Tests and build results are reported truthfully, with failures and warnings disclosed.
- No final logo approval, regulatory status, or live operational capability is claimed without proof.
