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


## Required UI source of truth — committed preview

The committed `design-preview/index.html` is the intended visual reference for the BIGWINZ interface, not merely an optional inspiration board. Use its layout, visual hierarchy, responsive behavior, surface treatments, typography, spacing, navigation patterns, event/odds presentation, bet-slip composition, wallet presentation, and overall premium visual direction as the baseline when upgrading the existing app.

Port the interface into the actual existing application routes and components. Do not simply leave the design in the standalone preview, produce another concept, or substitute a generic sportsbook template. Match the preview closely while adapting components to the app's real framework and existing data flows. Keep the existing approved product behavior and connect each visual element to real existing state and APIs.

The preview contains illustrative/sample content and a non-submitting bet slip. Treat that content as visual demonstration only: do not copy sample fixtures, odds, balances, bets, promotions, or outcomes into production data, and do not make the preview's demo interactions appear to place real bets or move money. Preserve actual application integrations and clearly retain unavailable/sandbox states.

### Mandatory safe execution

- Inspect the complete current repository and identify the actual app source, framework, routes, and integrations before editing.
- If the app source is absent from this repository or cannot be accessed, stop before inventing or scaffolding a replacement. Report exactly what source is missing and request the correct app branch/repository or have the owner connect the source.
- Keep the standalone preview available at `design-preview/index.html` as the reference.
- Do not replace the approved interface with a new design or change the approved logo independently.
- Implement incrementally in the existing codebase, preserving backend, auth, payments, betting, data, and admin functionality.
- Run the available checks and report actual results. Commit the implementation to `main` only after reviewing the diff and verifying it does not remove existing functionality.


## Required BIGWINZ page checklist

Freebuff must inspect the actual repository routes first, then map every applicable item below to the existing page, route, component, or clearly mark it as absent/not in scope with a reason. Do not invent new product capabilities simply to tick a box. Do not mark a page complete based on a screenshot alone: verify navigation, responsive layout, real data/state wiring, loading/empty/error states, and relevant user actions. Preserve current architecture and functionality.

### Customer-facing pages

- [ ] **Home / Sports discovery** — featured sports, leagues, fixtures, clear navigation, and data-backed content.
- [ ] **Sports category pages** — sport-specific event listings, filters, and useful empty states.
- [ ] **League / competition pages** — competition details and associated fixtures, where supported.
- [ ] **Fixture / event details** — teams or participants, event information, markets, odds, and availability states.
- [ ] **Live events / live scores** — live status and score updates only from actual configured feeds; show unavailable states honestly.
- [ ] **Search and discovery** — find sports, leagues, and events using existing supported search behavior.
- [ ] **Bet slip** — selected outcomes, odds, stake entry, potential return calculation, validation, remove/clear, and explicit confirmation flow wired to actual backend behavior. No false success.
- [ ] **Bet placement result** — genuine accepted, rejected, pending, or failed responses with reference details where available.
- [ ] **My bets / open bets** — authenticated user's real bet records and current status.
- [ ] **Bet history / settled bets** — actual historical records and settlement status, without fabricated outcomes.
- [ ] **Wallet overview** — real available balance and ledger-derived activity, with currency clearly shown.
- [ ] **Deposit** — configured payment methods, amount validation, provider handoff/status, and honest pending/failure/sandbox states.
- [ ] **Withdrawal** — eligibility, destination and amount validation, applicable review states, and accurate status.
- [ ] **Wallet transactions / transaction details** — real references, timestamps, amounts, fees where applicable, and lifecycle status.
- [ ] **Promotions / offers** — only valid configured offers, terms, eligibility, and expiry information.
- [ ] **Notifications / inbox** — actual notification state, read/unread behavior, and empty/error states where supported.

### Authentication and account

- [ ] **Sign in** — existing authentication, validation, errors, and secure session behavior.
- [ ] **Registration** — existing onboarding fields, validation, consent, and account creation flow.
- [ ] **Verification / OTP** — existing verification provider and retry/expiry/error handling; do not bypass verification.
- [ ] **Forgot password / recovery** — secure recovery flow with non-revealing responses where appropriate.
- [ ] **Profile / personal details** — authenticated user's real details and supported edit/save behavior.
- [ ] **Preferences / settings** — existing notification, display, language, or other supported preferences.
- [ ] **Security settings** — existing password, session, device, or MFA controls only where implemented.
- [ ] **Responsible gambling** — accessible safer-gambling information and any existing limits, time-outs, or self-exclusion controls; do not claim controls that are not operational.
- [ ] **Sign out / session expiry** — reliable session termination and appropriate return/navigation behavior.

### Administration and operations (if present)

- [ ] **Admin sign in and authorization** — role-checked access; no exposure of admin functions to customers.
- [ ] **Admin dashboard** — real operational metrics and clear unavailable-data states.
- [ ] **User/account management** — existing search, review, and permitted actions with auditability.
- [ ] **Bet/event/market management** — only actual supported controls and data sources.
- [ ] **Wallet/payment operations** — transaction review and status visibility without unauthorized balance mutation.
- [ ] **Settlement / reconciliation** — existing controls, source records, audit trail, and safe exception handling.
- [ ] **Promotions management** — configured offers and permission-checked changes, if supported.
- [ ] **Risk / responsible-gambling operations** — existing flags, limits, review actions, and audit trail, if supported.
- [ ] **Roles / permissions** — least-privilege enforcement for any existing administrative roles.
- [ ] **Audit logs / system status** — available events and health information, with no secret exposure.

### Shared page states and interaction quality

- [ ] Consistent BIGWINZ typography, color tokens, spacing, surfaces, navigation, controls, and status treatments based on the committed preview.
- [ ] Responsive behavior across supported phone, tablet, and desktop widths.
- [ ] Working navigation, active states, back behavior, and deep links for existing routes.
- [ ] Loading, skeleton, empty, validation, success, pending, unavailable, and error states appropriate to each page.
- [ ] Accessible contrast, visible keyboard focus, keyboard operation, semantic labels, and usable touch targets.
- [ ] Reduced-motion support and restrained, purposeful transitions.
- [ ] No broken links, dead buttons, fake odds, fabricated balances, sample bets, false payment confirmations, or misleading live indicators.

### Verification and sign-off

- [ ] Produce a route-to-checklist mapping of existing pages, including any item marked absent, unsupported, or out of scope and why.
- [ ] Verify each applicable page at mobile and desktop sizes.
- [ ] Exercise existing end-to-end journeys: discovery → event → bet slip → genuine placement response; sign-in → wallet → deposit/withdrawal status; account settings and sign-out; and applicable admin workflows.
- [ ] Run the repository's available type checks, lint, tests, and production build; report exact commands and real outcomes, including warnings and failures.
- [ ] Review the final diff for removed routes, changed contracts, weakened authorization, altered payment/betting logic, secrets, or unintended data changes.
- [ ] Commit to `main` only after the source exists, implementation is complete for the applicable scope, checks are run, and the diff is reviewed. Report commit SHA and known limitations.
- [ ] If application source is still missing, do not create a substitute app or claim the checklist has been implemented; report the exact missing source and stop safely.
