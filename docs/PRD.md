# Catering PRD

**Last updated:** October 26, 2026 · **Status:** Draft for Diego and Kean review
**Owners:** Diego and Kean, co-founders. Kean leads the build; both work on it and make product decisions together.
**Repo:** d-dawgs/Catering (private) · local: ~/Desktop/Builds/Catering
**Source of truth:** This is the single requirements document for the Catering product. It replaces every earlier catering PRD draft. Anything specific to one restaurant lives in that restaurant's pilot or setup files, never here.

**Help any restaurant take catering orders that arrive complete and correct, without the owner on the phone or retyping them.**

## 1. Summary

Catering is software that restaurants use to take catering orders and run them.

- **Customers** get help deciding what and how much to order, either from a guided assistant or on their own, and submit a complete order.
- **Staff** get one place to review, change, schedule and prepare every order, across every location, without retyping it into other tools.

Everything that differs between restaurants (menu, prices, rules, brand, locations) is setup, not code. The same product serves an independent restaurant, a catering-first business and a multi-location group.

**Where it fits:** Catering is the first product in our suite of software for restaurants. Later products are out of scope for this document.

**Current state:**
- V1, a clickable prototype, has been built and shown to our first pilot restaurant.
- V2 is not built yet.
- The repo starts as a clean skeleton.

## 2. Context

### How catering ordering typically works today

1. A customer finds the restaurant's catering page. They order through a catering-ordering tool, or by phone or email.
2. The owner or a manager gets an email about the order and checks it for mistakes.
3. Someone retypes the order into a shared calendar or a kitchen sheet so it gets prepared.
4. If an item can't be made in time, the owner calls the customer to offer substitutes.
5. Staff prepare and deliver, or hand off for pickup, working from that retyped copy.

### What we learned

These are the problems behind the product.
- **Seen** means we heard it directly in discovery.
- **To validate** means we believe it but haven't confirmed it with more than one restaurant.

| # | Problem | Status |
| --- | --- | --- |
| P1 | Customers don't know how to start a catering order, so they call to ask. | Seen |
| P2 | Customers can't judge how much food to order for their guest count and worry about running short. | Seen |
| P3 | Owners lose time on short, repeated calls walking customers through ordering. | Seen |
| P4 | Orders get retyped from the ordering tool into calendars and kitchen sheets, which costs admin time and causes missed or wrong items. | Seen |
| P5 | Orders arrive too close to the event for some items, so the owner calls to offer substitutes. | Seen |
| P6 | Restaurants pay for catering tools that don't solve P1–P5 and don't connect to their other systems. | Seen |
| P7 | Order admin falls on the owner or their family; hiring someone just for it costs more than software. | Seen |
| P8 | These problems hold across independent, catering-first and multi-location businesses. | To validate |

**What restaurants already value in current tools, which we must keep:** easy order placement, customer profiles, back-and-forth messaging with the customer, and letting customers update orders until a cutoff.

**What owners want:**
- Automation is welcome only if it works reliably.
- A person stays reachable.
- The owner keeps control of exceptions.
- The goal is time back for customers and family, not removing the human touch.

### Domain notes

- **Catering and carryout are different jobs.** Carryout usually runs through the restaurant's POS (e.g., Square, Toast, Clover). Catering needs event details, larger quantities, lead times and back-and-forth.
- **Menus are sold in mixed units:** per serving, per person (plates and cutlery), per set (chafing dishes), per tray or per bottle. Quantities often have minimums and fixed increments, such as minimum 10 servings or sold by the dozen.
- **Lead time depends on order size and item type.** Published policies and an owner's real practice often disagree.
- **Dietary tags are labels, not allergen guarantees.**

### Who we're building for

All three types are supported from the first build.

| Type | What's different about them |
| --- | --- |
| Independent, owner-run restaurant | 1–3 locations, small staff; catering is one part of the business; the owner does most admin |
| Catering-first business | Caterers, ghost kitchens and shared-kitchen operators; catering is the main revenue; more orders, more custom events |
| Multi-location group or chain | Several locations sharing a menu; central admin plus location managers; orders must route to the right location |

## 3. Goals and non-goals

### Goals

1. **Customers can place a complete catering order without calling.** Why: P1, P3.
2. **Customers know how much food to order.** Why: P2.
3. **Orders reach the kitchen and calendar without retyping.** Why: P4, P7.
4. **Lead-time problems are caught before submission, not by a phone call after it.** Why: P5.
5. **Staff stay in control of exceptions.** Nothing is confirmed or changed without the right person's approval. Why: owners accept automation only when it works.
6. **Any restaurant, with any number of locations, can be set up without code changes.** Why: this is a product for many restaurants, not a custom build.
7. **Do more than a restaurant's current catering tool, for less.** Why: P6.

### Non-goals

- A restaurant website or marketing tool
- Carryout or everyday online ordering
- A POS, payroll, inventory or delivery-dispatch system
- An AI that replaces the owner's judgment. It drafts; staff decide.
- A phone or voice agent, for now

## 4. Success measures

Each restaurant gets a baseline before its pilot, and targets are agreed with the owner.

**Success metrics**

- Orders completed with no staff retyping (target: all)
- Catering help calls per week
- Admin time per order
- Share of catering orders placed online, and share built with the assistant
- Monthly cost compared with the restaurant's current catering tool

**Guardrail metrics** (must not get worse)

- Wrong or missing items on orders
- Orders needing a substitution call
- Customers who start an order but don't submit
- Staff time spent in the tool compared with the old process

**A pilot succeeds when** the restaurant's catering orders run through the product without staff recreating them by phone or email, and the owner chooses to stop using their previous tool.

## 5. Users

- **Customer (event organizer):** an office admin ordering lunch or someone hosting a party or event. Orders occasionally, often on a phone.
- **Returning customer:** reorders, edits an order, checks status, messages the restaurant.
- **Owner/admin:** sees every location, approves orders and exceptions, manages menu, prices, rules and staff.
- **Location manager:** runs orders and settings for their assigned locations.
- **Kitchen/operations staff:** need accurate prep details and the schedule; update preparation status.
- **Setup operator (us at first):** sets up a new restaurant. This could become restaurant self-service later.

## 6. Scope and ownership

| Customer side | Staff side | Restaurant setup |
| --- | --- | --- |
| Guided or manual ordering | Action center | Brand |
| Quantity help | Orders list and detail | Locations |
| Location choice | Calendar | Menu and prices |
| Review and submit | Prep sheet | Ordering rules |
| Account: drafts, active, past | Messages | Fulfillment |
| Messages | Settings | Policies |
| Edit and cancellation requests | Analytics by location | Roles, alerts, integrations |

- **Who builds it:** Kean leads the build. Diego contributes design, product and review. Product decisions are made by both.
- **Brand:** customer pages wear each restaurant's logo and colors. The staff workspace uses one product design shared by every restaurant.
- **Relationship to restaurant websites:** a restaurant's website links to the customer entrance. The product shares no code, logins or data with any website.

## 7. Customer and staff journey

1. A customer opens catering from the restaurant's website or a direct link.
2. If the restaurant has several locations, the customer picks one for pickup, or the delivery address routes the order to the right one.
3. They choose guided or manual ordering, and can switch at any time without losing anything.
4. They enter event details: date and time, guest count, pickup or delivery (with address), contact info, dietary needs, budget and notes.
5. They build the menu with quantity help: coverage for the guest count, and warnings when the order looks short.
6. The product checks the location's rules. When something fails, it explains why and offers the alternatives the restaurant allows, or a person.
7. They review and submit.
8. They get a confirmation, and the same order appears in that location's staff queue and the owner's all-locations view.
9. Staff review it: accept, decline with a reason, ask a question, or propose a change for the customer to approve. An owner can reassign it to another location.
10. The customer sees drafts, active and past orders, messages the restaurant, requests edits or cancellation, and approves staff changes.
11. The order appears on the location's calendar and prep sheet. Staff mark it in preparation, then complete.

## 8. Restaurant setup

Setup has two levels: what applies to the whole business, and what each location can override.

**Business level**

| Area | What it holds | Example |
| --- | --- | --- |
| Brand | Name, logo, colors, fonts, assistant name, website link | Assistant named "Ask [Restaurant]" |
| Menu catalog | Categories, items, descriptions, photos, serving size and unit, dietary tags, options, base prices | 6 oz serving; sauce choice on wings |
| Quantity rules | Minimums and increments per item or category | Appetizers min 10 servings; desserts by the dozen |
| Portion guidance | Servings per guest by category; buffer % | 1 entrée serving per guest, +10% buffer |
| Add-ons | Supplies such as plates, cutlery, serving utensils, chafing sets | Plates and cutlery priced per person |
| Event details | Event types, required fields, dietary options shown | Corporate lunch, private party, wedding |
| Policies | Edit and cancellation cutoffs; whether submitting auto-confirms the order | Cancellation requests up to 72 hours before |
| Assistant | Approved prompts and answers; who customers contact for help | Fallback contact email and phone |
| People and roles | Owner/admin, location managers, staff; who gets which alerts | Owner gets every new order |
| Integrations | Calendar, email, payments, POS | Google Calendar |

**Location level** (overrides the business defaults)

| Area | What it holds |
| --- | --- |
| Basics | Name, address, contact, time zone |
| Menu availability | Which items are offered here; price overrides |
| Fulfillment | Pickup and/or delivery, delivery zones and fees, days and time windows |
| Lead times | Default, by guest count, by item or category; daily cutoff time |
| Money | Order minimum, tax rate, fees |
| Calendar and staff | Which calendar orders sync to; assigned managers and staff |

Two checks apply to every restaurant:
- A new restaurant or location can be set up by changing setup only.
- Setup is checked when it loads. Anything missing, such as an item with no price, is flagged to staff and never guessed for customers.

## 9. Requirements by version

### V2 — High-fidelity demo

**Learning goals** (tested with the pilot restaurant)

1. Does the owner think the assistant's suggested orders are right for their food? What would they correct?
2. Which steps would their customers still call about?
3. Does the staff view cover everything they currently retype into a calendar? What's missing?
4. Do the setup tables in section 8 capture their real rules, or does something not fit?
5. Will they run a live pilot, and on what terms?

**Constraints**

- Orders and drafts live in app memory and clear on reload or restart; no browser storage.
- No payment collection and no card fields.
- No AI provider, email or calendar connection; the assistant is scripted.
- Role views (owner, location manager, staff, customer) can be switched for the demo. This is not access control, and the product never says it is.
- No "demo" or "assumed data" labels in customer copy, and no claim that an email, payment or calendar action happened.
- Only approved setup data. No invented prices, portions, fees, policies or dietary claims.

**Customer**

- Branded entry from setup, with a link back to the restaurant's website
- Location choice, or automatic routing by delivery address when there are several locations
- Event and contact form; fields come from setup
- Manual menu: categories, descriptions, dietary filters, and quantity controls that enforce minimums and increments
- Scripted assistant:
  - A fixed set of approved prompts; it proposes a full order with a reason for each item
  - Apply, edit or keep each suggestion; switching to manual keeps everything entered
  - Allergy, availability, price and policy questions get a safe answer plus a way to contact the restaurant
- Quantity help (coverage and short-order warnings, labeled as guidance)
- Supplies and add-ons
- Rule checks with plain explanations and allowed alternatives
- Review and submit. The price breakdown appears only when every price is set; otherwise it says the restaurant will confirm pricing.
- Confirmation with order reference and next steps
- Account: drafts, active and past orders; order detail; messages; edit request; cancellation request; approve staff changes; contact profile (no passwords)

**Staff**

- Action center for new orders, messages and change/cancellation requests
- An all-locations view for owners and a per-location view for managers and staff
- Orders list with flags: short notice, large party, custom request, missing info
- Order detail with every action in section 7, location reassignment, and a full timeline
- **Statuses:** Submitted (only where staff accept first), Confirmed, Awaiting customer approval, Awaiting customer response, In preparation, Completed, Cancellation requested, Cancelled, Declined
- Per-order messages
- In-app calendar, filterable by location
- Printable prep sheet per order, plus daily totals by item per location
- Modest analytics: orders by status, upcoming events, by location
- Settings are view-only

**Setup**

The demo runs with three sample setups and no code changes between them:
- The pilot restaurant
- A sample catering-first business
- A sample business with two or more locations

**Build order**

1. Manual order, with the same order appearing in the staff queue
2. Locations and roles
3. Scripted assistant
4. Account, messages and changes
5. Calendar, prep sheet and analytics

**Out of scope for V2:** database, logins, payments, real AI, email, calendar sync, editable settings.

### V3 — Live pilot

**Learning goals**

1. Do calls and admin time actually drop in real use?
2. Do customers finish orders online without help?

**Requirements**

- A database, with each restaurant's data kept separate
- Logins:
  - Customer, owner, location manager and staff, with permissions checked on the server
  - Guest checkout, then a way to claim an account later
- Email notifications: customer confirmations and staff alerts, routed by location and role
- Calendar sync (Google Calendar first): orders and changes appear on each location's calendar automatically. This is the top-priority integration.
- Owners and managers can edit menu, prices, availability and lead times (within their role) without a developer
- Reliable hosting with backups; no duplicate submissions; clear errors and retry
- Runs alongside the restaurant's current catering tool first, then replaces it

**To decide during the pilot:** payments in the app, and a real AI assistant (section 11).

### V4+ — More restaurants

- An onboarding checklist, so new restaurants and locations are set up from setup only
- Deployment model decision (section 11A), pricing, and payments if needed
- Explore POS integrations and a real AI assistant if not already added
- Build validated items from section 13

## 10. Assistant rules

- **V2 is scripted:** a restaurant-approved set of questions and answers only.
- **Real AI comes later, only after the scripted version is approved.** It answers only from the restaurant's setup. Its suggestions are always editable, and its conversation is saved with the order. The restaurant approves sample answers before it goes live.
- **It always hands off to a person** for allergies, availability, price exceptions, policy questions and anything outside its setup.
- **It never** promises allergen safety, invents items, prices or policies, or confirms an exception.

## 11. Approaches and tradeoffs

**A. Deployment model**

| | Option 1: Separate copy per restaurant | Option 2: One shared platform restaurants sign up for |
| --- | --- | --- |
| Pros | Simple to build; each restaurant fully isolated; easy to customize; sells naturally as a custom product | One place to update; cheaper to run at scale; self-serve sign-up possible |
| Cons | Every update deployed many times; costs grow per restaurant | Harder security and data separation from day one; more to build first |

Selected: **not decided.** Option 1 is the working assumption for V2–V3. To keep Option 2 possible:
- Every record carries a business ID and a location ID.
- Setup loads per business rather than being built in.
- There are no restaurant-specific code paths.
- Each business has its own secrets.

Decide before V4.

**B. Locations**
- One setup per location: simple, but menus and rules are duplicated and drift apart.
- One business setup with location overrides: shared menu and policies, with local differences.

Proposed: business setup with location overrides (section 8).

**C. Order confirmation**
- Submit confirms immediately: certainty for the customer, but staff decline or change orders after the fact.
- Staff accept first: more control, but slower for the customer.

Proposed: a setting each restaurant chooses.

**D. Assistant**
- Scripted first: predictable, free and safe, but limited.
- Real AI first: handles any question, but costs money and can be wrong.

Selected: scripted for V2. Real AI is decided after a restaurant approves the scripted answers.

**E. Payments in a pilot**
- In-app payments: smoother, but needs a provider, fees and refund rules.
- The restaurant's current method: nothing new to build, but the order and the payment stay separate.

Proposed: the current method during pilots; revisit for V4.

**F. The restaurant's current catering tool**
- Complement it: lower risk, but the restaurant pays for and checks two tools.
- Replace it: one system and cost savings, but a failure means lost orders.

Proposed: run alongside during a pilot, then replace once the owner is confident.

## 12. Acceptance criteria

| ID | Requirement | Done when |
| --- | --- | --- |
| CAT-R01 | Independent product | Builds, runs and deploys from its own repo, with no code or styles from any restaurant website. |
| CAT-R02 | Branded customer entry | Customer pages use the restaurant's brand from setup and link back to its website. The staff workspace uses the product design. Brand colors that fail contrast are adjusted for text and buttons. |
| CAT-R03 | Setup-driven | The three V2 sample setups run with zero code changes between them. No restaurant name or restaurant-specific value appears in product code. |
| CAT-R04 | Locations | Orders route to the right location by the customer's choice or delivery address. Each location's menu availability, fulfillment, lead times and calendar come from its setup. Owners see all locations; managers see theirs. |
| CAT-R05 | Two paths, one order | Guided and manual produce the same editable order. Switching keeps all details. |
| CAT-R06 | Quantity help | Coverage and warnings come from the restaurant's portion guidance and are labeled as guidance. |
| CAT-R07 | Rules enforced | Minimums, increments, lead times, order minimum and zones block or flag with a plain explanation and the allowed alternatives. |
| CAT-R08 | One record | The customer's submission and the staff view show the same reference and fields. Edits and reassignments update that order and never create copies. |
| CAT-R09 | Controlled changes | Customer edits wait for staff approval; staff proposals wait for customer approval. The confirmed order stays unchanged until approved. Cancellation is a request with no refund promise. Unanswered orders stay visible for staff to decide. |
| CAT-R10 | Staff workspace | Action center, orders, detail actions, timeline, calendar and prep sheet all work from the same order data, by location. |
| CAT-R11 | Assistant safety | Allergy, availability, price and policy questions go to a person. The assistant states nothing that isn't in setup. |
| CAT-R12 | Honest status | No "sent," "synced" or "paid" unless the real action succeeded. Demo role switching is never presented as security. |
| CAT-R13 | Access control (V3) | Customers see only their own orders. Staff see only their locations. Settings changes respect role. All of this is enforced on the server and tested with direct URLs and requests. |
| CAT-R14 | Restaurant isolation (V3+) | Each restaurant's data, credentials and setup are separate. Setting up a new restaurant copies no other restaurant's records or secrets. |
| CAT-R15 | Accessible and mobile | The customer flow is fully usable on a 390px phone and by keyboard, with WCAG 2.2 AA contrast. |

## 13. To validate with pilots

Common catering features we haven't heard from a restaurant yet. Each moves into requirements only after a pilot confirms the need.

- Deposits and invoices (pay later, net terms for companies)
- Tax-exempt orders (schools, nonprofits)
- Recurring orders (weekly office lunches) and one-click reorder
- Company accounts with several people ordering
- Several drop-off times or addresses in one order
- Individually labeled boxed meals (name and dietary needs per box)
- Custom quotes or proposals for full-service events, including staffing, rentals and tastings
- Daily capacity limits per location (maximum orders or guests)
- Gratuity and service charges
- Contracts or e-signature for large events

## 14. Out of scope

- **Restaurant websites and marketing:** a separate kind of product.
- **Carryout ordering:** restaurants already handle it in their POS; catering is the gap.
- **Delivery dispatch and driver tracking:** a different problem, and not raised in discovery.
- **Inventory, purchasing, payroll and staffing:** handled by other systems.
- **AI phone agents:** discovery favored in-app help, and catering call volume is too low to justify one.
- **Importing data from other catering tools:** restaurants enter their menu through setup.

## 15. Timeline and risks

**Timeline:** no estimates yet. Team goal (Nov 15 roadmap): a product in real use by a client. V3 needs a database, logins, locations and calendar sync, so V3 by November 15 is ambitious.

**Risks**

- **Most catering evidence comes from a single pilot restaurant.** Problems may not hold for catering-first businesses or chains (P8).
- **Supporting all three restaurant types from day one makes V2 and V3 bigger.** Locations and roles are in the first build order to surface this early.
- **The pilot restaurant's rules may be unconfirmed when V2 is shown.**
- **A pilot restaurant may not commit to a live pilot or to paying.**
- **Wrong portion or allergen guidance from the assistant would damage trust.** Section 10 guards against this.
- **V3 means handling real customer data with a two-person team,** which needs security care.
- **Switching off a restaurant's current tool too early could lose orders,** so it runs in parallel first.

## 16. Open decisions

| Decision | Notes | Owner | Needed by |
| --- | --- | --- | --- |
| Product name | "Catering" is a working name | Diego + Kean | Before selling to a second restaurant |
| Deployment model | Section 11A | Diego + Kean | V4 |
| Customer and staff URLs | e.g., catering.[restaurant domain] for customers; staff login on the same deployment | Diego + Kean | V3 |
| Database, login, hosting and email providers | Kean proposes | Diego + Kean | V3 |
| AI provider and guardrails | Only after scripted answers are approved | Diego + Kean | V3 |
| Payments | Section 11E | Diego + Kean | Each pilot |
| Pricing to restaurants | Benchmark against what pilot restaurants pay today | Diego + Kean | Before pilot pitch |
| Location roles detail | Exactly what managers vs staff can change | Diego + Kean | V2 |
| Validate P8 and section 13 | Talk to a catering-first business and a multi-location group | Diego + Kean | V4 |

## 17. Decision log

- **Oct 25:** Combined PRD v0.4: scripted assistant, in-memory prototype, no payments or integrations.
- **Oct 26:**
  - Catering split from the restaurant website into its own product and repo (Diego + Kean).
  - Catering is universal, with no customer-specific content in this PRD.
  - Diego and Kean co-own it.
- **Oct 26:** Diego chose the following; Kean confirms in review:
  - One codebase with a separate deployment per restaurant for now; long-term model open
  - Customers see the restaurant's brand, staff see the product's
  - V2 demo, then V3 live pilot
  - Independent, catering-first and multi-location businesses all supported from day one
  - Pilot-specific details live in separate pilot docs
  - Unvalidated features go in a "to validate" list

## 18. Sources

- Discovery notes from restaurant meetings (Obsidian: Clients), abstracted into section 2
- Pilot docs in this repo (docs/pilots/) for customer-specific evidence, setup and rules
- Combined PRD v0.4, page checklist, V1 walkthrough and V1 product strategy, for earlier product decisions
- PRD format: combined PRD v0.4 and the Spec Doc example (Obsidian: Internal Strategy/Templates)
