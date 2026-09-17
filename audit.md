# Audit Report — Aadi Jain Portfolio (Session 9)

**Project files:** `index.html`, `style.css`
**Audit method:** mechanical, via [`audit.py`](./audit.py) — pattern-matching on the actual file text, not a judgment call. Re-run the script any time the files change; this document is a snapshot of one run, not a standing guarantee.
**Result of this run:** 11 of 12 checks pass. 1 fails.

---

## Results

| # | Requirement | Result | Evidence |
|---|---|---|---|
| 1 | Exactly one `<h1>`, containing "Aadi Jain" | ✅ PASS | `<h1>Aadi Jain</h1>` — one match, exact text |
| 2 | About section present | ✅ PASS | Element with `id="about"` found |
| 3 | Exactly the 5 required skills | ✅ PASS | Prompt Engineering, AI & ML, EDA, ML Model Development, Data Visualization — all present |
| 4 | Both required projects present | ✅ PASS | Student Attrition Prediction, NoBrokerage.com Chatbot — both present |
| 5 | HTML and CSS kept in separate files | ✅ PASS | `style.css` exists, linked via `<link rel="stylesheet">`; no embedded `<style>` block in `index.html` |
| 6 | No inline CSS | ✅ PASS | Zero `style="..."` attributes found |
| 7 | No JavaScript | ✅ PASS | No `<script>` tags, no `on*=` event-handler attributes, no `javascript:` URIs |
| 8 | Visible hover effects | ✅ PASS | 3 `:hover` rules defined in `style.css` |
| 9 | Responsive around 375px | ✅ PASS | 3 `@media` queries, including one at `max-width: 380px` |
| 10 | Professional, deliberate colour scheme | ✅ PASS | 3 hex values in `:root` (`#16302B`, `#F5F6F4`, `#B8862B`) — count confirmed mechanically; visual coherence still worth an eyeball check |
| 11 | No invented email / GitHub / social links | ✅ PASS | No email, GitHub, LinkedIn, Twitter/X, Instagram, or phone-number patterns anywhere in `index.html` |
| 12 | No leftover placeholder text | ❌ **FAIL** | Two instances of `"Project description to be added."` still in the file |

---

## The one open issue

Both project entries — **Student Attrition Prediction** and **NoBrokerage.com Chatbot** — still contain placeholder text instead of real descriptions. This dates back to the earlier fix that removed invented project details; the placeholders were left in deliberately as a flag, but they were never replaced with your real content.

**This is the only thing standing between this project and a clean pass.** Fix it, re-run `audit.py`, confirm all 12 checks show PASS, and the deliverable is done.

---

## What this report is, and isn't

- It confirms **structure and constraint compliance** — file separation, absence of forbidden techniques, required content present, no invented contact info.
- It does **not** confirm visual quality, whether the palette actually reads as cohesive, or whether the site is well-written. Those need your own eyes, because they're not mechanically checkable.
- A PASS here is evidence, not a certificate. If you change the files after reading this, re-run the script — this document does not update itself.

---

## Reality check

You now have three layers doing the same job for different reasons: the live chat exchange where I explained a fix, the script that checks it mechanically, and this document that records one run of that script. That's not redundant — it's the difference between *a claim*, *a repeatable test*, and *a paper trail*. But don't let the existence of all three become a reason to stop checking yourself. The fastest way to fail a grading rubric is to trust a green checklist you haven't personally reread against the original spec at least once.
