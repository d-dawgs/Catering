# Catering — agent instructions

This repository is the independent catering product. Diego owns the repository; Kean leads implementation. Customer and staff experiences belong here. Do not edit the public website repository.

## Start here

- Read README.md, docs/CONTEXT.md, docs/BUILD_PLAN.md and docs/DESIGN.md.
- The PRD is intentionally absent while Diego compares drafts. Once the merged product PRD is supplied, check its approval state with Diego/Kean before implementing feature scope. Do not import or publish a PRD on their behalf.
- Follow design-first, bounded task briefs and owner review. Inspect current changes and preserve unrelated work.

## Product and data boundaries

- One reusable codebase, separate deployments per restaurant for now. Design restaurant-specific branding/catalog/rules/configuration separately from generic workflows. Do not choose a shared multi-restaurant service architecture silently.
- The public website's Catering marketing page will link to the customer entrance here. This product must not depend on a marketing-site shell or another repository's source.
- Current `/` and `/staff` are empty skeletons, not functioning ordering or authenticated software. Do not claim V2 features exist.
- Keep route files thin when features are introduced; use TypeScript and plain scoped CSS. No unapproved component library or database/auth/payment/email/calendar/AI provider.
- Do not invent prices, portions, availability, dietary guarantees, policies, sample customer records or credentials. Menu references are dated research. Resolve prototype assumptions and production policy conflicts explicitly.
- Before real data/live use, enforce customer ownership and staff authorization server-side and verify direct requests, not only hidden navigation. No real orders/payments/integrations or live credentials without separately approved activation.
- Do not modify sibling products, install dependencies, mutate Git, commit/push, deploy, invite collaborators or delete source unless the current task authorizes it. Initialization authorization does not carry into future tasks.

## Verification

Run npm run lint, npm run typecheck and npm run build for application changes; add meaningful behavior/access checks as actual features are implemented. Report results and limitations; do not fix unrelated areas or mark future work complete. Product owners review acceptance.

<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->
