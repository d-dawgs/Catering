# Catering context

## Confirmed product split and reuse

Diego owns the independent Catering repository; Kean leads implementation. Both customer and staff experiences belong here. Pearl-web owns the public business website, including a Catering marketing page whose button opens the separate software. Staff should enter the software directly rather than navigate through marketing pages.

One reusable codebase, separate restaurant deployments for now. Pearl Island is the first deployment. No shared multi-restaurant service, auth/database/provider or detailed configuration/data design is selected by the skeleton.

## Current state and PRD gate

Kean presented V1 and has not built V2 yet. This repo has only blank customer/staff canvases and no functioning orders/accounts/access controls/integrations.

The Catering PRD was added on October 27, 2026 as docs/PRD.md, a draft for Diego and Kean review. It is universal and names no customer. Pearl Island specifics live in docs/pilots/pearl-island.md. The build-plan screen inventory is candidate planning context to reconcile with the PRD.

## Important unresolved business/operating decisions

The final PRD must distinguish prototype assumptions from Sober-confirmed production rules. Earlier sources conflict on calendar-day versus business-hour/day lead times and cancellation handling. Prices, minimum order value, delivery zones/fees, required fields, supplies, time zone/cutoff, confirmation/payment policy, account claiming, staff roles/statuses, no-response handling and integrations remain to reconcile. No numeric policy is silently enforced in the skeleton.

The retained menu reference contains dated descriptions/caveats, not a live orderable catalog, verified prices or allergy guarantees. Scripted guidance, customer changes/messages, calendar and analytics are future scope candidates. Before real business orders/data, durable storage, appropriate server-side access controls, recovery and operational ownership require separate design/activation review.

Source provenance: Diego's October 26, 2026 product/reuse decisions; earlier combined planning snapshot `fbf758f3aad2f8e927f680408b1fc6ed49c0d3f1` and dated V1/workflow research. That snapshot's PRD prose claimed an order/staff implementation while its code/README were blank; do not copy the completion claim. No runtime/source dependency on the legacy repository exists here. Original client notes remain in Obsidian.

Current: standalone skeleton. Next: owner review and merged PRD before V2 feature design. Initial setup Git operations were explicitly authorized; later commits/pushes/deployments/deletion require their own instruction. Collaborator invitations and live domains/services are not part of initialization.
