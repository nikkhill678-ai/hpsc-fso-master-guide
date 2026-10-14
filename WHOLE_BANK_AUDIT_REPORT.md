# Whole Question Bank Audit — All Six Units

**Audit date:** 2026-10-15  
**Scope:** all six current 150-question JSON banks integrated into the existing static study site. Unit 3A and 3B remain combined in Unit 3. Unit 2 is the bank built against the newly designated authoritative 149-page manual.  
**Important:** this is an automated whole-bank structural and similarity audit plus an explicit item-level verification register. It is **not** a claim that a human has independently verified every scientific or legal fact in all 900 questions.

## Results at a glance

- Total questions scanned: **900**.
- Expected distribution: **150 per unit; 50 easy, 50 medium, 50 hard**.
- Structural issues detected: **0**. (See `WHOLE_BANK_STRUCTURAL_ISSUES.csv`; zero rows means no structural flags under these checks.)
- Similarity/duplicate candidate records: **147**. These include exact duplicate stems/IDs and cross-difficulty stem-similarity flags; similarity is a triage heuristic, not proof of redundancy.
- Every question is explicitly marked in the register as **not yet certified** by a full manual scientific review. Legal review is pending wherever applicable.
- Current bank-level disclaimer is preserved verbatim in the website quiz experience and catalogue.

## Per-unit scan

| Unit | Questions | Easy | Medium | Hard | Cross-difficulty similarity candidates | Items needing human scientific review |
|---|---:|---:|---:|---:|---:|---:|
| 1 | 150 | 50 | 50 | 50 | 2 | 150 |
| 2 | 150 | 50 | 50 | 50 | 1 | 150 |
| 3 | 150 | 50 | 50 | 50 | 0 | 150 |
| 4 | 150 | 50 | 50 | 50 | 14 | 150 |
| 5 | 150 | 50 | 50 | 50 | 0 | 150 |
| 6 | 150 | 50 | 50 | 50 | 130 | 150 |

## What the automated audit checks

1. JSON parses for all six banks.
2. Expected bank count and difficulty split.
3. Unique IDs within each bank.
4. One stem, four option objects, unique option labels, exactly one keyed answer that matches an option.
5. Explanation/solution and source-basis fields exist.
6. Scoring metadata is +1 / −0.25 / 0.
7. Exact repeated stems and cross-difficulty question-stem similarity candidates are logged.

## Whole-bank regulatory/numeric claim triage (automated keyword flags)

These are deliberately broad keyword flags, not confirmed errors or a legal review. Terms such as “limit”, “standard” and ordinary scientific numbers can be false positives. Every flagged item requires human/source verification; items without flags may still contain legal or numeric claims.

| Unit | Regulatory/standards keyword flags | Numeric/threshold keyword flags |
|---|---:|---:|
| 1 | 66 | 150 |
| 2 | 33 | 150 |
| 3 | 23 | 150 |
| 4 | 143 | 150 |
| 5 | 150 | 150 |
| 6 | 141 | 150 |

The two flags are now included as columns in `WHOLE_BANK_AUDIT_REGISTER.csv`. They prioritise the 900-item manual review but do not replace it.

## What this does not prove

- The answer key is factually correct or uniquely defensible.
- A distractor is unambiguously wrong in every interpretation.
- The explanation faithfully represents the source page.
- Any statutory limit, regulation number, penalty, date, additive permission, labelling rule, packaging migration limit or residue limit is current.
- The three difficulty tiers measure different cognitive demand; a wording similarity scan cannot assess that fully.

## Regulatory source currency

FSSAI's official notifications pages show ongoing 2026 changes, including packaging amendments (10 August 2026), contaminants/toxins/residues amendments (25 May 2026), labelling amendments (30 March 2026), licensing amendments (12 March 2026), and laboratory/sample-analysis amendments (18 September 2026). Consequently, all law-dependent MCQs need question-specific checking against the relevant final Gazette notification and its commencement date. The official notifications portal is the index; for legal conclusions, the applicable notification text and effective date govern. Sources: [FSSAI notifications](https://www.fssai.gov.in/notifications.php), [FSSAI current notifications page](https://fssai.gov.in/food-law/notifications?csrt=1134053321848574512&notification=ordinary-notification), [FSSAI product standards](https://fssai.gov.in/standards/product-standards?pr=1).

## Item-level workflow recommended

Use `WHOLE_BANK_AUDIT_REGISTER.csv` as the master ledger. Review each row against its named source text and, where legal/current, against primary notification text. Record a precise citation (section/regulation/paragraph/page and effective date), decision (`verified`, `revise`, `remove`, or `not applicable`), and reviewer/date. Do not silently substitute general knowledge for a source gap. Maintain the required draft disclaimer until that work is complete.

## Required draft disclaimer (preserved verbatim)

> This is a draft, not a fully audited final mock. The difficulty levels currently reuse some underlying concepts, so redundancy and question discrimination need review. Scientific and current regulatory verification also remains pending. The questions are not represented as actual HPSC previous-year questions.
