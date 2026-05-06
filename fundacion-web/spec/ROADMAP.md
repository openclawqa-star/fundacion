# Fundación Un Plan Con Café, Delivery Roadmap

## Goal
Launch a mobile-first donation platform that turns homepage traffic into completed donations, while supporting projects, events, stories, and purpose-driven products.

## Jira tracking
- Master roadmap: `SCRUM-5`
- Product decisions: `SCRUM-6`
- Frontend MVP: `SCRUM-7`
- Backend and donations: `SCRUM-8`
- QA, deployment, and launch: `SCRUM-9`

## Current state
- Homepage prototype exists in HTML and CSS.
- Core product decisions are still open.
- No backend, database, payment integration, admin tools, or tests exist yet.

## Phase 1, Close product decisions
1. Decide the donation flow behavior, modal, dedicated page, or external redirect.
2. Choose the payment provider, Stripe, MercadoPago, or other.
3. Decide donation modes, one-time only or recurring too.
4. Define the MVP content model, projects, stories, events, products, and metrics.
5. Decide whether authentication is needed in v1.
6. Define whether an admin panel is required for launch or deferred.
7. Decide product inventory scope, static catalog or managed stock.
8. Define legal, trust, and contact requirements for donation checkout and footer.

## Phase 2, Finish the frontend MVP
1. Refine the homepage copy and CTA behavior around the chosen donation flow.
2. Build a real donation entry experience, modal or page.
3. Build project listing and project detail views.
4. Build product listing and product detail views.
5. Build events listing and event detail views.
6. Add media and story presentation components.
7. Add trust elements, FAQ, footer, contact, and confirmation states.
8. Add JavaScript for interactions, form handling, and validation.
9. Improve accessibility, mobile responsiveness, and performance.

## Phase 3, Build backend foundation
1. Create the FastAPI project structure.
2. Define the relational database schema.
3. Add environment and configuration management.
4. Create REST endpoints for projects, stories, events, products, and impact metrics.
5. Create donation endpoints and webhook handling.
6. Add persistence, validation, and error handling.

## Phase 4, Implement donations end to end
1. Integrate the selected payment provider.
2. Build donation session creation and status tracking.
3. Add success, failure, and cancellation flows.
4. Add donor confirmation behavior, receipt email and or thank-you page.
5. Add reporting fields needed for impact transparency.

## Phase 5, Add content operations
1. Decide whether content is file-based, admin-managed, or hybrid.
2. If admin is required, build a minimal admin interface for projects, stories, events, products, and metrics.
3. Add content publishing workflow and basic auditability.

## Phase 6, Quality, deployment, and launch
1. Add unit and integration tests.
2. Add end-to-end donation journey tests.
3. Set up CI checks and deployment pipeline.
4. Prepare production configuration and secrets.
5. Run final QA on mobile-first flows.
6. Launch and monitor donations, errors, and conversion.

## Recommended execution order
1. Finish Phase 1 first.
2. Run Phase 2 and Phase 3 in parallel once the donation direction is decided.
3. Start Phase 4 as soon as backend foundations are stable.
4. Treat Phase 5 as MVP-only if content updates must be self-serve at launch.
5. Keep Phase 6 running continuously, with the launch gate at the end.

## Highest priority blockers right now
- Donation flow decision
- Payment provider decision
- MVP data model definition
- Admin scope decision
