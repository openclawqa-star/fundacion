# Fundación Un Plan Con Café, Product Decision Checklist

Jira decision tracker: `SCRUM-6`

## Goal
Resolve the open product choices that block backend and donation implementation.

## Decision 1, Donation flow
**Question:** What should happen when the user taps `Donar ahora`?

Options:
- Modal
- Dedicated donation page
- External provider redirect

**Recommendation:** Dedicated donation page.

Why:
- better mobile focus
- easier analytics and testing
- cleaner place for trust, amount selection, and provider handling
- avoids modal complexity during payment flows

## Decision 2, Payment provider
**Question:** Which provider will process donations?

Options:
- Stripe
- MercadoPago
- Other

**Recommendation:** MercadoPago if the primary donor base is in Latin America, Stripe otherwise.

Why:
- local payment fit matters more than engineering preference
- provider choice affects checkout UX, backend endpoints, and webhooks

## Decision 3, Donation type
**Question:** Should MVP support one-time only, or recurring too?

Options:
- One-time only
- One-time and recurring

**Recommendation:** One-time only for MVP.

Why:
- faster launch
- fewer billing edge cases
- simpler reporting and customer support

## Decision 4, MVP content model
**Question:** Which entities are required for launch?

Recommended MVP entities:
- Projects
- Impact metrics
- Stories or media entries
- Events
- Products
- Donations

## Decision 5, Authentication
**Question:** Is login required in v1?

Options:
- No public auth, admin only
- Public user accounts plus admin

**Recommendation:** No donor accounts in MVP, admin access only.

Why:
- lowers friction on donations
- reduces complexity and security surface

## Decision 6, Admin scope
**Question:** Is an admin panel required for launch?

Options:
- No, content managed manually
- Yes, minimal admin for core content

**Recommendation:** Minimal admin only if the team needs frequent updates before launch, otherwise defer and manage content manually first.

## Decision 7, Product inventory
**Question:** Should products use static or dynamic stock in MVP?

Options:
- Static catalog, no inventory logic
- Dynamic stock tracking

**Recommendation:** Static catalog for MVP unless stock changes daily.

## Decision 8, Legal and trust requirements
Define before implementation:
- donation receipt behavior
- thank-you page requirements
- refund or contact policy
- privacy policy and terms
- foundation identity and contact details in footer

## Suggested order
1. Donation flow
2. Payment provider
3. Donation type
4. Authentication
5. Admin scope
6. MVP content model
7. Inventory scope
8. Legal and trust requirements

## Proposed next milestone
Once Decisions 1 to 4 are approved, move immediately into frontend donation UX and backend donation integration.
