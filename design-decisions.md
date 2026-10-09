# Design Decisions — v2 (Oct 7, 2026)

How the wireframe (`index.html`) applies the research in `research-findings.md`.

## Structure

Six iPad screens, 1194×834 landscape, 3-column NavigationSplitView (sidebar · main · agent inspector):

1. **Today** — day dashboard, in-progress Visit resume, scheduled Visits with Past Context on each row, Next Best Actions.
2. **Accounts** — browse-first (filter chips as primary; search is a secondary voice-enabled affordance). Suggested-for-today row + Your HCPs grid. Each card shows last-touch summary.
3. **HCP record** — no tabs. Stacked cards: Highlights (Last Visit promoted) → Next Best Actions → Identity → Products → Interactions → Inquiries → Samples & Consent.
4. **Visits** — day-grouped list (In Progress, Today, Tomorrow). Group visits distinguished with 👥 chip.
5. **Visit record** — All-Actions SPA. Mode toggle 1:1 / Group. Highlights with Past Context, then one card listing every action for the visit (Content · Products · Samples · DTP · Marketing · Inquiry · Compliance · Close-out).
6. **In-Visit modal** — mode-aware:
   - **1:1:** Single Page (No Side Panel). All sections scrollable with a floating jump-nav chip top-right.
   - **Group:** Side-panel attendee navigator on left + per-attendee Single Page. Side-panel ↔ card-swipe toggle for A/B comparison.

## Research → design mapping

| Research signal | What the wireframe does |
|---|---|
| Flat beats sequential | Step rail removed. In-Visit is a scrollable Single Page. |
| "All Actions" SPA preferred | Visit record lists every action in one place — no "+ Add action" step. |
| Avoid tab layouts per record type | HCP and Visit records use stacked cards, no segmented controls. |
| Continuity on provider profile | Last-visit summary promoted into Highlights (above the fold) on HCP and Visit records. |
| Attendee rollup is top pain | Group Visit mode has side-panel attendee navigator with signature/decline rollup counts. |
| Group visits are massive scale | Voice-first per-attendee capture pattern ("Dr. Shah signed, materials standard set, no notes") called out explicitly. |
| Entry-path consistency | Breadcrumbs always route through Accounts/Visits, affordances identical regardless of path. |
| Visit-First | "+ Start a Visit" is the primary CTA on Today and on every HCP record. |
| Voice-First | Persistent 🎙 mic on toolbar, every form field, every inspector input, agent commands. |
| Past Context auto-display | Highlights card on HCP + Visit records shows last-visit date and auto-summary. |
| Next Best Actions | NBA block on Today, HCP, Visit, and inside the In-Visit modal. Agent inspector leads with NBAs, not generic suggestions. |

## Known gaps / future work

- **Buyer control of left panel** — not prototyped (admin config pattern, hard to show statically).
- **Card-swipe validation** — toggle is present but behavior isn't modeled; needs real test harness.
- **Offline conflict handling** — the "offline-safe · auto-saved" label is a hint, not a resolved flow.
- **CLM Library** — surfaced as a nav item but no deep screen.
- **Tasks / Insights** — nav stubs only.

## Deliberate rejections

- Figma (user prefers tangible HTML iterations).
- Step rail / wizard navigation.
- Grid layout for attendees in group visits (rejected by reps in concept testing).
- Search-first HCP finding (users want to browse cards, not type).
