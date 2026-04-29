# Quarterly microcopy audit — 2026-04-29

## Versions at time of run
- Microcopy spec: v1.0 (Notion last-edited 2026-04-29) — derived from positioning v2.24, canonical highlights v1
- Positioning doc: v2.24 (Notion last-edited 2026-04-28)
- Canonical highlights: v2.1 (Notion last-edited 2026-04-29)

---

## Findings

### Drift findings (slot-by-slot)

**SAFE CUTS / REPLACEMENTS APPLIED IN THIS BRANCH**

| File:line | Slot class | Current | Rule violated | Action taken |
|---|---|---|---|---|
| `index.html:331–335` | `.hero-trust` | `IF / THEN / BECAUSE · Field rules · not wiki` | §2.2 — feature-pills, no named/dated proof point; §3 — `wiki` in user-visible text | **CUT** — entire `.hero-trust` element removed |
| `for-ai-agents.html:249–255` | `.hero-trust` | `MCP-native · IF / THEN / BECAUSE · Attribution built in` | §2.2 — feature-pills, no named/dated proof point (this exact row is cited in §2.2 as "Fail — already cut") | **CUT** — entire `.hero-trust` element removed |
| `for-product-managers.html:223` | `.hero-eyebrow` | `For Product Managers` | §2.1 — pure audience label; §3 — `For [audience]` as hero eyebrow | **REPLACED** with canonical category-frame: `The layer between your team's expertise and your product's decisions` (§2.1 option a; §4 approved phrase) |
| `for-ai-agents.html:237` | `.hero-eyebrow` | `For agent builders` | §2.1 — pure audience label; §3 — `For [audience]` as hero eyebrow (spec §1 intro explicitly names this finding as "All cut") | **REPLACED** with canonical category-frame: `The layer between your team's expertise and your product's decisions` (§2.1 option a; §4 approved phrase) |

---

**EDITORIAL JUDGMENT REQUIRED — flagged only, not auto-applied**

| File:line | Slot class | Current | Rule violated | Suggested replacement |
|---|---|---|---|---|
| `for-ceos.html:254` | `.hero-eyebrow` | `The reasoning layer` | §2.1 — incomplete; closer to a label than a positioned category-frame or judgment-work line. No FAIL match in §2.1's example list, but does not meet either pass criterion (a) or (b). Compare with passing bar: "Stop encoding business logic" names the work; "Your expertise, made permanent" names the value. "The reasoning layer" is an object-label, not a value or work statement. | Option (a): `The layer between your team's expertise and your product's decisions`; or a new CEO-specific line naming the judgment work (e.g., the moat-compounding angle from §7 open question). Needs editorial pass. |
| `pilot.html:196` | `.hero-eyebrow` | `Be a founding partner` | §2.1 — invitation/branding frame, not a category-frame or persona judgment-work line. Closer to "Welcome to FieldRules" (§2.1 FAIL: branding) than any passing example. | Option (a): `The layer between your team's expertise and your product's decisions`; or a pilot-specific line naming what the pilot delivers (e.g., `Govern AI decisions from day one`). Needs editorial pass. |

---

### Forbidden phrase findings

**REQUIRES EDITORIAL JUDGMENT — flagged only, not auto-applied**

| File:line | Phrase found | Context | Rule | Suggested replacement |
|---|---|---|---|---|
| `index.html:562,569,576,583,590` | `Learn more →` | In `.who-card-arrow` divs inside `<a class="who-card">` anchor elements (user-visible text in navigational CTAs) | §3 — `Learn more` in CTAs | Replace each instance with a card-specific directional phrase. The AI Agents card already models the correct pattern: `See the integration model →`. Each card needs its own equivalent (e.g., `See the PM workflow →`, `See the attribution model →`, etc.). Needs editorial pass per card. |
| `for-engineers.html:282` | `knowledge base` | `.section-lede`: "A knowledge base is searched; a skill graph is traversed—by domain, by author, by BECAUSE chain." | §3 — `knowledge base` banned even in contrast ("gives it oxygen") | Remove the first clause entirely: `A skill graph is traversed—by domain, by author, by BECAUSE chain.` OR rephrase the contrast without naming the banned category: `Document stores are indexed. A skill graph is traversed.` Needs editorial review for surrounding paragraph fit. |
| `for-ceos.html:292` | `knowledge base` | `.paradox-body`: "A knowledge base is searched. A skill graph is traversed. What your competitors can buy is the interface." | §3 — same rule | Same options as above. Removing the first sentence ("A knowledge base is searched.") preserves the argument and eliminates the banned phrase. Needs editorial review. |
| `for-ai-agents.html:339` | `policy docs` | `.contrast-title` in the "Adjacent category" contrast card: "Pull together your SOPs, support scripts, KB articles, and policy docs." | §3 — `policy doc` banned (plural form `policy docs` matches) | This instance describes the competitor/adjacent category, not FieldRules output. However, §3 applies categorically. Replace with: "Pull together your SOPs, support scripts, and KB articles." (simply removing `policy docs` from the enumeration keeps the competitor description intact without the banned term). Needs editorial sign-off since it changes competitor characterisation. |

---

### Spec drift

**Canonical highlights version gap (queued spec-diff):**

The microcopy spec v1.0 was derived from `canonical-highlights-v1`. The canonical highlights document has since been updated to **v2.1** (April 29, 2026), adding 10 new lift-and-use phrases sourced from competitive framing v4.11. These phrases are **not yet in spec §4**. They should be incorporated in the next spec revision:

Phrases in canonical-highlights-v2.1 not yet in spec §4:

1. `Every sprint, PMs ship features against business logic they can't verify.` *(positioning v2.24 — PM pain statement)*
2. `Every AI governance tool tells you what rules exist. FieldRules is the only one that tells you whether your rules are actually thinking.` *(positioning v2.24 — Reasoning Health Score one-liner)*
3. `Mid-market B2B SaaS companies are publicly a software product and privately a consulting firm.` *(story map v3.8 — story opener)*
4. `If you didn't design [the layer between your team's expertise and your AI] deliberately, the model fills it in from training data: the industry average, the generic case — not your specific operational logic.` *(story map v3.8 — consequence statement)*
5. `AI-generated rationale will be cheap, scalable, and the first thing to fail in an audit.` *(story map v3.8 — regulatory framing)*
6. `The companies that deploy AI well are the ones that built the layer before they needed it.` *(sales motion v2.13)*
7. `A documentation sprint three months from now captures what people think they do. FieldRules captures what they actually do, at the moment they're doing it.` *(sales motion v2.13 — contrast line)*
8. `If it doesn't surface things you didn't know were there, we don't ask you to extend.` *(sales motion v2.13 — pilot close)*
9. `If your two most senior CSMs left tomorrow, what would happen to the judgment they apply to edge cases?` *(sales motion v2.13 — Sam discovery opener)*
10. `When you're speccing a feature that touches [domain X], how do you know the business logic is right before it ships?` *(sales motion v2.13 / positioning v2.24 — canonical PM opening question)*

**Positioning doc:** v2.24 matches what spec was last revised against. No positioning-driven spec-diff at this time. Next version bump (v2.25+) will require a trigger-based diff pass per §6.

---

## Pages with no findings

- `for-domain-experts.html` — all audited slots pass; no forbidden phrases in visible body text
- `for-researchers.html` — all audited slots pass; no forbidden phrases in visible body text

---

## Changes applied in this branch

```
index.html             — removed .hero-trust feature-pill row (lines 330–335 incl. DEV comment)
for-ai-agents.html     — replaced .hero-eyebrow "For agent builders" → canonical category-frame
for-ai-agents.html     — removed .hero-trust feature-pill row (lines 249–255)
for-product-managers.html — replaced .hero-eyebrow "For Product Managers" → canonical category-frame
```
