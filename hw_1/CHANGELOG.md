# Prompts Changelog — PayPilot

All notable changes to system prompts and overlays are documented in this file.

---

## [v1.1] - 2026-09-15

### Added
- **R-1 Fix**: Added strict constraint prohibiting hallucinated fee percentages if tool/RAG context lacks figures (Section 3).
- **R-2 Fix**: Enforced mandatory pre-check via `check_dispute_eligibility` before confirming dispute capabilities to customers (Section 4 & 5).
- **R-3 Fix**: Explicitly defined arithmetic consistency formula for FX breakdown outputs: $\text{Final amount} = \text{Amount} \times \text{Rate} - \text{Spread}$ rounded to 2 decimal places (Section 7).
- Added explicit prohibition against mentioning internal compliance terminology (`compliance_hold`) to customers (Section 5).

### Fixed
- Fixed contradiction where agent was previously permitted to answer fees "from memory" if tool results were empty.
- Fixed D25 defect overlay by explicitly prohibiting artificial rounding of final FX amounts up to the nearest hundred.

### Removed
- Removed ambiguous wording in role description regarding general empathy; narrowed down empathy requirement strictly to the first sentence during loss/fraud reports.

---

## [v1.0] - 2026-09-08

### Added
- Initial baseline prompt (`base.v1.md`) for PayPilot customer support stand.