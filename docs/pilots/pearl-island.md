# Pearl Island — Catering Pilot

**Last updated:** October 26, 2026 · **Status:** Draft for Diego and Kean review
**Owners:** Diego and Kean
**Destination:** Catering repo, `docs/pilots/pearl-island.md`
**How this relates to the PRD:** The Catering PRD is universal and is the source of truth for what the product does. This doc holds only what is specific to Pearl Island as our first customer and pilot: their evidence, setup and rules, and the pilot plan. If something here would change the product for every restaurant, it goes into the PRD in general terms.

## 1. About Pearl Island

- **Who:** Sober Pierre and Zakiah Pierre (owners). Caribbean catering plus Pearl Island 2 Go carryout, run from the B.E.A.C.O.N. shared kitchen, 221 Carlton Road, Charlottesville. No dine-in.
- **Business type in PRD terms:** independent, owner-run, catering-first leaning. Sober wants to grow catering.
- **Tools today:**
  - Spoonfed for catering ordering ($235/month, renewed monthly; a per-order fee is unconfirmed)
  - Square for carryout, POS, payroll, contracts and email blasts to past customers
  - Google Calendar for prep
- **Status:** saw the V1 demo on Oct 20 and is interested in continuing. No pilot, pricing or purchase commitment yet.

## 2. Their current catering workflow

1. The customer finds the catering page on pearlislandcatering.com, creates a Spoonfed profile and orders.
2. Sober and admins get an email notification.
3. They check the order in Spoonfed for discrepancies and view it on Spoonfed's calendar.
4. Sober's wife manually re-enters the order into Google Calendar.
5. Staff prepare and fulfill from that.
6. If an item can't be made in time, Sober calls the customer to offer alternatives.

## 3. Evidence behind the PRD's problems

| PRD problem | What Pearl Island told us | Source |
| --- | --- | --- |
| P1 Don't know how to start | Customers' most common question is "how do I cater?" | Oct 20 |
| P2 How much food | Repeated serving-size questions; Sober adds a 10–15% buffer from experience | Oct 6 |
| P3 Time on calls | About 5–6 calls a week at 5–7 minutes, including outgoing substitution calls (approximate). Volume is low right now because business is slow. | Oct 20 |
| P4 Retyping | His wife re-enters every Spoonfed order into Google Calendar | Oct 20 |
| P5 Short notice | Sober calls to offer substitutes when an item can't be made in time | Oct 20 |
| P6 Tools | Open to leaving Spoonfed for more functionality, a smoother experience and ideally lower cost | Oct 20 |
| P7 Admin labor | He'd need to hire someone at $18–25/hour for this admin work; Spoonfed is cheaper than that | Oct 20 |

**What Sober values in Spoonfed:** easy order placement, customer profiles, communication with customers, and easy order updates.

**What he wants:** automation "as long as it works," and a person available. He wants to be more technology-centered and to have more time for family and customers. He liked an AI-built order with a manual option, and preferred in-app help over a phone agent.

## 4. Pearl Island setup

These values come from public sources and V1. None are confirmed by Sober yet.

| Setup area | Pearl Island values |
| --- | --- |
| Brand | Logo; turquoise #00A1CA with darker teal; assistant name "Ask Pearl"; link back to the new Pearl-web site |
| Locations | One (the shared kitchen) |
| Menu | Matched menu reference: items in both the 2026 menu and the website-linked menu, with descriptions (`docs/references/menu-reference.md`) |
| Prices | Spoonfed prices observed Oct 13 (e.g., entrées $5.00–$6.25 per 6 oz serving). Unconfirmed; not to be shown as final. |
| Quantity rules | Appetizers min 10 servings; wing bites min 25; cold box meals and salad lunches min 10 per type; desserts min 12, in 12s |
| Serving units | 6 oz spoon servings; plantains 2 per serving |
| Options | Wing flavors: Jerk, Island Rub, Mango-Pineapple, Tamarind, BBQ |
| Add-ons | Spoonfed supply list: plates/cutlery/cups, cutlery packs, serving spoons and tongs, disposable chafing sets (prices unconfirmed) |
| Fulfillment | Pickup confirmed; delivery and zones to confirm |
| Dietary tags | Vegetarian, Vegan, Gluten-free, Dairy-free (labels only) |
| Event types | Corporate lunch observed in V1; others to confirm |

## 5. Rules to confirm with Sober

- Item prices, and who keeps them updated
- **Lead times.** The sources conflict:
  - The earlier brief says 2 calendar days, or 3 for more than 50 guests.
  - The Spoonfed storefront says 5 business days for more than 50 guests.
  - Spoonfed's terms say 48 business hours for traditional orders and 72 for custom items, appetizers and box lunches.
  - The cutoff time and time zone are also unknown.
- Delivery availability, zones, fees and time windows
- Order minimum, tax and fees
- Payment timing and method
- Cancellation cutoff and fee; refunds (the 72-hour cancellation request is provisional)
- Supplies list and prices
- Whether submitting confirms the order (assumed in v0.4) or staff accept first
- What staff do when a customer doesn't reply
- Portion guidance per guest, and the buffer he uses
- Assistant scripts, and who customers contact for help
- Who on staff gets which alerts and roles (Sober, his wife, staff)

## 6. Pilot plan

**V2 demo for Sober**
- Show the full journey with Pearl Island's setup.
- Collect corrections and confirm the rules in section 5.
- **Next step:** schedule the next in-person meeting (October roadmap goal: book it by Oct 31).

**Before V3**
- Walk through a real Spoonfed order and the Google Calendar re-entry with Sober's wife.
- Capture which fields she copies, how long it takes, how often it happens, and how changes and cancellations are handled.

**V3 live pilot**
- Runs alongside Spoonfed, then replaces it.
- Payments stay with Pearl Island's current method during the pilot.
- The website's "Start a catering order" button switches from Spoonfed to the product when the pilot starts.

**Baseline to capture before V3**
- Catering help calls per week (current estimate about 5–6)
- Time his wife spends per order on calendar re-entry
- Orders per week
- Order errors and missed items
- Substitution calls
- Spoonfed cost ($235/month, plus any per-order fee)

**Pilot success:** catering orders run through the product without staff recreating them by phone or email, and Sober decides to turn off Spoonfed.

## 7. Pilot risks

- Business is slow right now, so measured savings may look small.
- Sober hasn't committed to a pilot or to paying, and pricing hasn't been discussed.
- His wife's process hasn't been observed directly; it's known from Sober's description.
- The lead-time rules conflict, so the wrong rule could block or allow orders.

## 8. Sources

- Obsidian: Clients/Active/Pearl Island
  - Meetings 10-06-2026 and 10-20-2026
  - About/Updates (Oct 14 priorities)
  - Business Model
  - Contacts
  - Plan/Next Steps
- Combined PRD v0.4 and menu reference (pi2go: playbook/)
- Spoonfed workflow notes, Oct 13 (restaurant_demo)
- V1 prototype walkthrough, Oct 25 (pi2go: playbook/PROTOTYPE_WALKTHROUGH.md)
