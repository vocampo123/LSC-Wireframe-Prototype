# Research Findings — LSC Rep Visit Navigation

Synthesized from user research shared Oct 2026. Two sources: (1) general navigation research across journey mapping, Insights group-visit concepts, AFLS Mobile Strategy; (2) Comparative Visit SPA Data Analysis & Findings (Aug 2025).

---

## Signal 1 — Flat beats sequential

In concept testing, field reps preferred simpler/flatter navigation over multi-step/grid structures. For group visit data intake, reps strongly preferred a **Side Panel** approach and rejected the Grid outright. _(Insights Group Visit Concepts, Feb 2026)_

**Design implication:** No step wizards. Flat section layouts in Visit screens.

---

## Signal 2 — "All Actions" SPA preferred over "Add Actions" SPA

From the Comparative Visit SPA study: users clearly prefer the **"All Actions"** SPA over the "Add Actions" SPA. "Add Actions" looks "clean" but has terrible usability.

Why users like "All Actions":
- **Saves clicks** — faster task completion
- **Guides workflow** — reminds users of needed steps without extra effort
- **Keeps tools accessible** — everything in one place

Recommendation: Prioritize the **"All Actions" SPA** — either the current design or the **Single Page (No Side Panel)** version. The "All Actions" family is the only SPA that consistently scores favorably in standalone tests.

**Design implication:** Every action on the Visit record visible on one page in logical order. No "+ Add action" step.

---

## Signal 3 — Avoid tab-based layouts per record type

As seen in Call 2.0: tab-based layouts per record type add unnecessary work and fragment the workflow.

**Design implication:** Record pages (HCP, Visit) use stacked cards, not segmented controls / tabs.

---

## Signal 4 — Continuity on the provider profile

Reps want the last call date + notes/summary visible directly on the HCP profile, not drill-back through records. Pause-bottleneck in AFLS Mobile Strategy Research (Apr 2026): reps delay entering accounts because key info isn't easily accessible.

**Design implication:** Promote "last touch" (last visit date + one-line summary) into HCP Highlights above the fold.

---

## Signal 5 — Attendee rollup is the top VOC pain

No rollup for Visit attendees → reps manually drill into Child Visits related list; a Flow workaround causes double-sync issues on iPad. **Priority: High.**

**Design implication:** Attendee rollup on parent Visit record is a first-class concern.

---

## Signal 6 — Group visits are massive scale

Lunch-and-Learns are the most common group scenario — daily cadence, up to 80+ attendees. Reps rarely revisit group call data afterward.

**Design implication:** Group visit flow optimized for speed per attendee (voice-first helps here).

---

## Signal 7 — Entry-path consistency matters at the functionality level

Logged defect: the "New Insight" quick action fails when a Visit is opened via Account → Related List nested nav, but works via direct tab access.

**Design implication:** Every entry path into a Visit record must produce identical affordances.

---

## Future direction (from Comparative SPA study)

- **Visit-First system** — shift away from account-first workflow; the visit is the starting point.
- **Voice-First Interface** — voice-to-text to reduce admin burden. Holistic across the app, not one-off.
- **Immediate, In-App Value:**
  - **Past Context** — auto-displayed summaries of previous visits.
  - **On-Click Future Guidance / Next Best Actions** — intelligent recommendations for discussion points, follow-ups, and content.
- **Buyer control of left panel** — admins choose which record types appear and how many.

---

## Proposed-but-unvalidated patterns

- **Card-swipe between child-visit records** of different attendees (eliminates returning to parent). Design proposal from Dec 2025 planning session — flagged save-triggered delay tradeoff; no user validation.

In the current wireframe (v2), card-swipe is offered as a toggle alongside the validated Side Panel in Group mode so both can be shown in testing.
