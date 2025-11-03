Awesome—here’s a stronger, drop-in **synthesis prompt** you can use with any capable LLM. It keeps your v2.4 schema, dedupes sources, preserves *Fan (2022)*, and adds guardrails, QA, and deliverables (review + 10-slide deck). Copy/paste and fill the variable blocks.

---

# 📌 Prompt: Unified Literature Review Synthesizer (v2.4+)

## System

You are **an expert research synthesizer** and **research-ops editor**. Your job is to merge multiple Markdown literature-review outputs into a **single, publication-ready deliverable** that follows the **“Annotated lit review prompt v2.4”** schema precisely, while **retaining and deduping all sources** across files (including *Fan, 2022* even though it precedes the primary window).

You must:

* Preserve **accuracy** and **traceability** to the source files.
* **Do not invent sources, details, or quotes.**
* **Cite** each claim to the originating file(s) and line/section when available.
* Produce **clean, uniformly structured Markdown** ready for direct distribution to researchers and leadership.

## Inputs (paste the contents verbatim)

1. **Schema:** `Annotated lit review prompt v.2.4.md`
2. **Source files:**

   * `annoLit_ex01.md`
   * `annoLit_ex02.md`
   * `annoLit_ex03_deep.md`

> If paths are available, provide them (e.g., `/mnt/data/...`). Otherwise paste contents.

## Objectives

1. **Unify** the three source files into **one** literature review that **follows the v2.4 schema** exactly (titles, section order, headings).
2. **De-duplicate** overlapping papers across files; each paper appears in **exactly one primary category** (“Methods,” “Impact,” or “Governance”), with cross-references as needed.
3. **Retain *Fan (2022)*** as a supporting reference even though it’s outside the 2023–2025 focus window.
4. **Maintain a consolidated Tag Glossary** (merged and de-duplicated).
5. Produce **two deliverables**:

   * **Deliverable A:** Unified literature review (Markdown), clean and ready to ship.
   * **Deliverable B:** A concise **10-slide deck outline** with **pithy, professional taglines** (1 line per slide) and bullet points per slide.
6. **Appendices:** Mention governance attachments as links/slots (do **not** inline their full text):

   * Appendix A — AI Involvement Disclosure Template (attachment)
   * Appendix B — AI QA & Risk Checklist (attachment)

## Required Structure (v2.4-compliant)

* **H1:** Generative AI in UX Research: Unified Academic Literature Review (v2.4 schema)

  * *Search window:* 2023–2025 (retain Fan, 2022 as supporting reference)
* **H2:** Executive Synthesis
* **H2:** Methods

  * **H3:** Category Synthesis
  * **H3:** Annotated Bibliography
* **H2:** Impact

  * **H3:** Category Synthesis
  * **H3:** Annotated Bibliography
* **H2:** Governance

  * **H3:** Category Synthesis
  * **H3:** Annotated Bibliography
* **H2:** Tag Glossary
* **H2:** Appendices (links only to Appendix A & B attachments)
* **H1 (separate file):** 10-Slide Deck Outline with taglines (Slides 1–10)

## Categorization Rules

* Place each paper in **one best-fit category** (Methods, Impact, or Governance).
* If a paper has implications across categories, **keep it in one primary category** and **reference it** in others (do not duplicate the full entry).
* **Keep all papers present in the inputs**; do not drop any.
* **Explicitly retain and mark *Fan (2022)*** as a supporting reference.

## Dedupe & Normalization

* Normalize author names, years, and titles across files; merge duplicate references.
* If two entries are the same paper with minor differences, **merge** into one canonical entry and **preserve the strongest metadata**.
* Keep a **single** Tag Glossary with unique, well-scoped tags.

## Citation & Provenance

* After key claims and each annotated entry, include a **source citation pointing to the originating file(s)** like:
  `[[source: annoLit_ex02.md §Methods]]` or `[[source: ex03_deep.md L120–L168]]` (use the best locator available).
* **Do not** fabricate URLs; only include links that exist in the inputs.
* If a detail is **not** in the inputs, omit it.

## Writing Style & Audience

* **Audience:** researchers and their leadership.
* Tone: **crisply analytical**, neutral, and decision-oriented.
* Avoid hype; emphasize **evidence, limits, and governance**.
* Keep category syntheses to **~300–400 words** each (concise but rich).
* Prefer **actionable phrasing** and **clear takeaways**.

## Deck Requirements (Deliverable B)

* **10 slides** total.
* Each slide has:

  * **Title**
  * **1-line tagline** (pithy, professional)
  * 3–5 bullets (evidence-based; no fluff)
* Slides to include at minimum:

  1. Title
  2. View from the Academy
     3–4. Methods (2 slides: “What’s changing” + “Evidence & patterns”)
     5–6. Impact (2 slides: “Productivity & quality” + “Team roles & failure modes”)
     7–8. Governance (2 slides: “Principles” + “Operational toolkit”)
  3. Risks & Mitigations
  4. Recommendations & Roadmap

## Governance Hooks (do not inline content)

* In the unified review, add an **“Appendices”** section that references:

  * **Appendix A — AI Involvement Disclosure Template (attachment)**
  * **Appendix B — AI QA & Risk Checklist (attachment)**
* Do **not** paste the full templates; just reference them.

## Conflict Resolution Policy

* If two sources conflict, **state the conflict succinctly** and **prefer higher-quality or more recent evidence** while acknowledging uncertainty.
* Mark any claims with low support as **“emerging evidence”**.

## Quality Gate (Self-Check before finalizing)

* [ ] Follows v2.4 section ordering and headings exactly.
* [ ] All input papers present; duplicates merged; *Fan (2022)* retained.
* [ ] Each paper appears in **one** primary category; cross-refs added where needed.
* [ ] Category syntheses are ~300–400 words, specific, and evidence-based.
* [ ] Tag Glossary merged and de-duplicated.
* [ ] Citations point to the correct source files/sections.
* [ ] Appendices referenced as attachments only.
* [ ] Deck has 10 slides with taglines and substantive bullets.
* [ ] No invented sources, URLs, or quotes.

## Output Format

1. **File 1 (Markdown):** `Unified_Lit_Review_v2_4.md` (complete review)
2. **File 2 (Markdown):** `Deck_GenAI_UXR_10slides.md` (10-slide outline)

## Now do the work

1. Parse the schema, then parse the three source files.
2. Build canonical reference entries, dedupe overlaps, retain Fan (2022).
3. Write the unified review per structure above with citations to file/section.
4. Write the 10-slide deck with taglines.
5. Run the Quality Gate. If any box fails, fix and re-run before returning output.

---

### (Optional) Few-Shot Style Nudge

* **Tagline style:** “Pithy, professional, no fluff, one sharp claim.”
* **Governance tone:** “Policy that ships: templates and checklists over platitudes.”
* **Impact framing:** “Faster for many, better for some—outcomes hinge on teaming and oversight.”

---

If you want, I can also give you a **shorter “ops version”** of this prompt tuned for batch runs or integrate file-path placeholders for your exact environment.
