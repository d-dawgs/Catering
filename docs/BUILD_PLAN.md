# Catering build plan

Status: independent blank skeleton; Ready for Diego review after initialization checks. Kean has not built V2. The merged PRD and first V2 slice require Diego/Kean review.

## Current and next

- Current: review the skeleton and compare the PRD drafts.
- Next: add the merged catering PRD, confirm the first-demo slice and map customer/staff screens.
- Completed product features: none. Empty `/` and `/staff` are structural entry points only.

## Dependency-ordered path

| Step | Work | Review check |
| --- | --- | --- |
| 1 | Review merged PRD and demo boundary | Diego/Kean agree intended behavior and what stays unbuilt; no implementation claims copied from the older PRD. |
| 2 | Validate rules and restaurant configuration | Menu/catalog, required fields, pricing, delivery/lead-time/cancellation conflicts and restaurant-specific versus generic structure are explicit. |
| 3 | Design customer/staff journeys | Desktop/mobile flows, screen content, states, staff entry and access boundaries are approved. |
| 4 | Approve first vertical-slice brief | Exact files, demo-state rules, confirmation semantics and checks are recorded before coding. |
| 5 | Build manual request → staff visibility | Approved event/contact, menu, review/submission and matching staff order view carry the same data. |
| 6 | Add approved customer capabilities | Draft/order views, profile, secure access and messages/change requests are introduced in bounded slices. |
| 7 | Add approved staff capabilities | Review/clarification/changes, status history and action items; calendar/analytics only if scoped. |
| 8 | Add scripted guidance if approved | Guided/manual paths preserve one editable order; no real LLM or external action is implied. |
| 9 | Validate reuse and product quality | Restaurant configuration, customer/staff access, data integrity, keyboard/mobile UX and technical checks are verified. |
| 10 | Separate live pilot/activation | Persistence, authorization, real integrations, Sober policies, training/support and release/rollback are agreed before accepting real business orders. |

## Screen inventory to reconcile with the merged PRD

This is retained planning context, not an approved replacement PRD or a frozen route map:

- Event/contact: contact name/email/phone, optional organization; event type/date/time/guests; pickup/delivery/address; optional dietary needs, budget and notes. Required rules/options remain to confirm.
- Menu: approved categories/descriptions/options, quantities/minimums/increments, reviewable summary and prices only when sourced. Supplies remain a separate scope question.
- Review/confirmation: review entered details, edit earlier steps, submit under the agreed prototype/production semantics and show the same request to staff.
- Customer area: drafted/active/past orders, order detail, requested edits/cancellation, linked messages and profile. Secure access must be designed; contact information alone is not authorization.
- Staff area: order list/detail, clarification, customer-edit review, staff proposals, cancellation decisions, status/activity history and messages/action items. Calendar, analytics and account/settings are later scope candidates.
- Guided path: finite approved prompts, editable suggestions, switch to manual preserving data, and human fallback for unsupported questions; include only if the merged PRD agrees.

The final PRD must resolve field rules, status vocabulary, approvals, prices/minimums/fees, cutoff/time zone, account access and live versus prototype behavior. Do not silently implement this inventory while that PRD is pending.

Track current/next/blocked/ready/accepted work as the product develops. Only the owners accept completion. No automatic Git, provider, deployment or old-repo deletion action follows from this plan.
