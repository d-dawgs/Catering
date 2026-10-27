# Catering design direction

Planning foundation for owner review. No V2 screens are built or approved by this document; the merged PRD must establish feature scope first.

- Customer ordering should make event details, menu quantities, review and the next action clear, with human help available when needed.
- Staff screens should make order details, status, pending customer/staff actions and event dates easy to scan. They are an operational product, not the marketing website's layout.
- Keep forms readable, keyboard-usable and responsive. Define empty/loading/validation/failure/confirmation states before feature coding; claim success only when the underlying action actually succeeds.
- Retain appropriate Pearl Island warmth and brand cues for its deployment. Keep restaurant-specific branding/catalog/rules configurable rather than mixing them into generic product structure. Final tokens/type/assets require owner review; the public website's five-token restriction is not automatically imposed on future staff screens.
- Prefer a clear manual flow; scripted guidance is optional scope pending the merged PRD. Never make unsupported dietary/availability/price assurances.
- Staff should have a direct workspace entrance. Authorization is implemented in the product's server-side behavior before real data, not by merely hiding navigation.
- Design the first complete customer-to-staff slice before building it. Record approved screen states, content, interaction and access checks in its implementation brief. Do not copy the old website's large display typography, decorative cards or loose spacing into dense operational forms by default.
