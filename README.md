# Catering

Standalone catering software for restaurant customers and staff. Repository owner: Diego Bartra. Implementation lead: Kean. Source: https://github.com/d-dawgs/Catering.

## Current state

An independent Next.js App Router, TypeScript and plain-CSS skeleton. `/` and `/staff` are intentionally empty white canvases. There are no orders, accounts, staff access controls, persistence or integrations. The staff path exposes no records and is not a working authenticated workspace.

**PRD pending:** Diego is comparing separate drafts, including one prepared with Claude, and will add the merged catering PRD later. No PRD or PRD placeholder file is included. Kean has not built V2 yet; planning notes are not evidence of implemented features or approval of a new feature scope.

## Local development

Use Node.js 20.9 or later supported by the pinned dependencies. From this repository:

```sh
npm ci
npm run dev
```

Use the printed localhost URL. `/` is the customer canvas; `/staff` is the staff canvas. Checks:

```sh
npm run lint
npm run typecheck
npm run build
```

`npm run start` serves a successful production build. No external service or environment variable is required yet. Generated output and dependencies stay ignored.

## Product boundary and reuse

Customer ordering/accounts and the staff workspace belong to this product. The public Pearl Island website is separate and will link here from its Catering marketing page. Staff should be able to enter their workspace directly when that experience is built.

Maintain one reusable software codebase with separate deployments per restaurant for now. Restaurant configuration and data boundaries require design before implementation. Do not clone customer data/secrets or Pearl Island assumptions into another restaurant's deployment. A shared multi-restaurant service is not the current target.

## Core documents and next step

- [Build plan](docs/BUILD_PLAN.md): proposed sequence and PRD gate.
- [Design direction](docs/DESIGN.md): operational UI principles.
- [Context](docs/CONTEXT.md): source and business-rule limits.
- [Menu reference](docs/references/menu-reference.md): dated descriptions, not a live catalog.
- [Agent instructions](AGENTS.md): repository-specific rules.

Next: review the skeleton and merged catering PRD with Diego/Kean before selecting V2's first vertical slice. No deployment, Spoonfed migration, real order collection or external integration occurs during initialization.
