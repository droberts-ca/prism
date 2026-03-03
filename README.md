# PRISM
**Participation Routines & Inclusive Supports Map**
*A structured observation guide for P/TK participation planning*

---

## What It Is

PRISM is a participation mapping tool for inclusive early childhood settings. It helps P/TK teachers document how a child's access to classroom activities shifts across contexts — and why — in language that IEP teams can use directly.

It is not an assessment battery. It does not produce scores or eligibility determinations. It produces structured participation documentation that informs IEP present levels and supports least restrictive environment reasoning.

**Use it when:**
- A child is being evaluated or receiving services in a P/TK setting
- The IEP team needs ecological data from the classroom teacher of record
- Present Levels need to describe participation patterns, not test-room performance
- The team is reasoning about LRE placement or supports

---

## How It Works

PRISM guides the teacher through an Observation section and a consolidated Domains section, then Synthesis.

**Observation** asks the teacher to:
1. Rate participation access across four classroom contexts (whole group, small group, free play/centers, transitions)
2. Select the best access context and most constrained context
3. Rank the primary environmental driver — what explains why participation shifts

**Domains** presents two indicator clusters aligned to PTKLF and DRDP:
- **Approaches to Learning — including Self-Regulation** (PTKLF ATL / DRDP ATL-REG), split into Engagement & Persistence and Self-Regulation subclusters
- **Social-Emotional Development** (PTKLF SED / DRDP SED)

The teacher checks indicators consistently observed. No re-scoring, no domain-level matrices — the Observation section already captured the ecological record.

**Synthesis** collects:
- Support profile — UDL/universal supports present vs. individually planned supports required
- Observation scope
- Optional teacher narrative notes

Hitting **Generate Participation Summary** assembles a Present Levels paragraph from the structured data using a local clause-module renderer — no API, no network connection required. Output includes a timestamped attribution footer.

---

## Renderer Logic

The renderer uses a three-layer hierarchy to build output:

| Layer | Signal | Source |
|-------|--------|--------|
| **1 — Participation Pattern** | Stable / context-dependent / individualized / high-support | Context matrix access column |
| **2 — Domain Asymmetry** | ATL-REG vs SED indicator density | Domain indicator counts |
| **3 — Subcluster Asymmetry** | Engagement vs Self-Regulation within ATL-REG | Subcluster indicator counts |

Each layer activates only when the layer above it justifies it. Divergence thresholds are calibrated by clinical reasoning — see inline code comments for rationale and recalibration guidance.

---

## Framework Alignment

| Framework | Connection |
|-----------|------------|
| **California PTKLF (2024)** | Organized around ATL and SED foundation areas; Self-Regulation nested within ATL per DRDP strand structure |
| **DRDP (CDE/WestEd)** | Domain structure maps directly to ATL-REG and SED strands; supports rating rationale documentation |
| **DRAccess (CDE)** | DRDP-to-Foundations linkage mirrors PRISM's two-lane observation-to-planning structure |
| **ECTA Preschool LRE Guidance** | Context contrast structure maps directly to ECTA LRE reasoning framework |
| **IDEA Part B / Indicator 6** | Ecological documentation supports defensible LRE reasoning and Indicator 6 placement decisions |

---

## Files

| File | Description |
|------|-------------|
| `index.html` | PRISM tool — open in any browser, works offline |
| `PRISM_Origin_Memo.docx` | Origin and intent memo — design rationale, intended/non-intended use, framework alignment |
| `README.md` | This file |

---

## Using PRISM

**No installation required.** Open `index.html` in any modern browser.

- Works offline — no internet connection needed after loading
- Autosaves to browser localStorage — form survives page refresh
- Student ID field accepts initials or anonymous identifier — no PII required
- Clear Assessment button resets all fields with confirmation

**For GitHub Pages:** the tool is live at the repo's Pages URL. Teachers can bookmark it directly.

---

## Versioning

`PRISM v1.1· February 2026`

Modifications should be versioned and re-documented to preserve alignment integrity. Fork this repo, increment the version stamp in the tool footer and README, and update the Origin Memo accordingly.

**v1.1 changes:** Collapsed ATL/SED/REG three-tab structure into two-lane ATL-REG/SED domain architecture aligned with PTKLF and DRDP strand structure. Removed AEPS-3 crosswalk. Rebuilt renderer with typed divergence logic, composed support sentences, conditional ecological framing, and three-layer domain/subcluster asymmetry detection.

---

## Developed by

FCUSD Special Education · Early Childhood Assessment Team (ECAT)
Folsom Cordova Unified School District

*Aligned with California PTKLF (2024) · DRDP ATL-REG & SED · ECTA Preschool LRE Guidance · IDEA Part B Indicator 6*
