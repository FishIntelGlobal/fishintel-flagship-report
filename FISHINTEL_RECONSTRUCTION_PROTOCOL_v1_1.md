# FishIntel Reconstruction Protocol

**Version:** 1.1  
**Effective:** April 2026  
**Status:** Active — applies to all reconstructions from Report 006 onwards  
**Supersedes:** Implicit v1.0 methodology documented in Flagship Reconstruction Manual v1.0  
**Origin:** Five-report forensic cross-verification audit conducted April 2026  

---

## Scope

This protocol governs environmental reconstruction using publicly available meteorological reanalysis data and information contained in published maritime accident investigation reports.

FishIntel reconstructions quantify the environmental conditions in which operational decisions were made. They do not determine liability, fault, or legal responsibility. They do not assign blame to any individual, organisation, or vessel operator. Their purpose is to establish what environmental conditions were objectively knowable before critical maritime decisions were made.

---

## Purpose

This document defines the standards, rules, and verification requirements for FishIntel environmental reconstructions. It codifies the practices developed across the first five published flagship reconstructions and incorporates findings from a full forensic audit of the published library.

Every FishIntel reconstruction must comply with this protocol. The protocol is versioned and changes are documented.

---

## 1. Extraction Window Discipline

### Rule 1.1 — Capture the Decision Environment

Every reconstruction must include ERA5 extractions that cover the period when the critical operational decision was made, not just the incident window.

If the MAIB report identifies a decision point (e.g., "the master decided to remain at anchor"), the extraction window must extend back to cover the environmental conditions at that decision time. The reconstruction must show what conditions were objectively knowable when the decision was made.

**Minimum extraction points:** 4 timestamps. Recommended: 5.

**Window coverage:** The extraction window must open no later than the first operational decision identified in the MAIB report. Where the decision time cannot be determined from the source material, the reconstruction must extend at least 6 hours prior to the incident. Where the MAIB identifies a specific earlier decision point (e.g., anchoring the previous evening), the window should extend to cover that decision.

### Rule 1.2 — Standard ERA5 Hours Only

All extraction timestamps must align with standard ERA5 hourly intervals (00:00, 01:00, 02:00, etc.). Reconstruction values must not be attributed to non-standard times (e.g., "05:25 UTC") without explicit labelling as the nearest-hour ERA5 extraction.

Format: `ERA5 05:00 UTC (nearest hour to 0525 grounding)` — not `05:25 UTC`.

### Rule 1.3 — Post-Event Extraction

At least one extraction timestamp after the incident is permitted (to show the environmental trend through the event) but must be labelled as post-incident.

---

## 2. Source Discrepancy Handling

### Rule 2.1 — Transparent Divergence

When ERA5 values diverge from MAIB-stated values, the divergence must be:
- Explicitly stated with both values presented
- Quantified (e.g., "divergence of approximately 0.65 m")
- Explained with physically plausible mechanisms
- Not minimised or dismissed

**Best practice (from Flagship 002):** Present both values as lower and upper bounds of the actual condition. State the ERA5 value as the gridded estimate and the MAIB value as the local observation, and use both in the analytical assessment.

### Rule 2.2 — Every MAIB Environmental Parameter Must Appear

If the MAIB casualty information table states an environmental parameter (wind, sea state, tidal stream, visibility, water temperature, darkness), it must appear in the reconstruction — either as an ERA5-derived value or as a MAIB-sourced citation.

Omitting a MAIB-stated environmental parameter is not acceptable. If ERA5 cannot provide the parameter, cite the MAIB value with explicit sourcing.

### Rule 2.3 — Wind Direction Precision

When the MAIB states a cardinal wind direction (e.g., "south-west"), the reconstruction must note any difference between the cardinal approximation and the ERA5 precise bearing. A difference of >15° between stated and reconstructed direction must be flagged.

---

## 3. Threshold and Classification Language

### Rule 3.1 — Threshold Tags Must Be Factually Accurate

Classification tags (e.g., "EXCEEDS," "WITHIN," "BELOW") must accurately describe the relationship between the measured value and the threshold.

- If a value is within a defined band: tag as "WITHIN [band name]"
- If a value exceeds the upper limit of a band: tag as "EXCEEDS [band name]"
- If a value is at or near a threshold boundary: tag as "AT [threshold] BOUNDARY"

**Prohibited:** Tagging a value as "EXCEEDS" when it falls within the stated range.

### Rule 3.2 — Wolfson Threshold Ranges

When citing Wolfson stability thresholds that have high and low limits (e.g., from blanketing/interaction effects), both limits must be presented as a range. Using only the high or low limit without stating the range is not permitted.

### Rule 3.3 — Uncertainty Acknowledgement

When ERA5 values are within the uncertainty range of a threshold comparison (e.g., SWH exceedance of 0.02 m against a threshold where ERA5 uncertainty is ±0.2 m), the report must state that the exceedance is within the uncertainty bounds and cannot be determined with statistical confidence.

---

## 4. Duration and Exposure Claims

### Rule 4.1 — Source-Verified Claims Only

Claims about the duration of operations (e.g., "four hours of continuous manual shooting") or cumulative exposure (e.g., "1,440 deployment cycles") must be sourced from the MAIB report or clearly labelled as estimates.

If the MAIB does not state the duration, the reconstruction must use qualified language: "The reconstruction window spans [X] hours. The MAIB report does not confirm the duration of continuous operations within this period."

### Rule 4.2 — Estimate Labelling

Calculated values derived from assumptions (e.g., deployment rate × assumed hours) must be presented as bounded estimates with the assumptions stated, not as factual statements.

---

## 5. Foreseeability Statements

### Rule 5.1 — Forecast Evidence

Foreseeability claims must be grounded in one of:
- A specific MAIB statement that the forecast was consulted and conditions matched (strongest)
- The synoptic-scale nature of the reconstructed conditions (moderate)
- Actual forecast products referenced by date and issuing authority (strongest possible)

**Prohibited:** Stating conditions "would typically appear in standard marine weather forecasts" without either (a) the MAIB confirming the forecast was available, or (b) presenting the actual forecast product.

### Rule 5.2 — Foreseeability vs Forecast Accuracy

If ERA5 reconstructed conditions exceed the forecast described in the MAIB report (e.g., conditions exceeded the F8 forecast), this must be explicitly stated. Foreseeability at the forecast level is different from foreseeability at the actual-conditions level.

---

## 6. Data Tiering

### Rule 6.1 — Three-Tier Evidence Classification

All data in a reconstruction must be classified into one of three tiers:

| Tier | Source | Evidence Status |
|---|---|---|
| **Tier 1** | ERA5 pipeline output, unit-gated, hash-sealed | Primary evidence. Enters the cryptographic evidence chain. |
| **Tier 2** | Pipeline-derived analysis (risk scores, T_irr, Beaufort classification) | Derived evidence. Traceable to Tier 1 inputs through deterministic logic. |
| **Tier 3** | MAIB-sourced values, contextual observations, assumptions | Contextual evidence. Does not enter the Tier 1 evidence chain. Must be attributed. |

Every value, table entry, and claim in the report must be identifiable as Tier 1, 2, or 3.

### Rule 6.2 — Stability Data Classification

Wolfson stability data, freeboard measurements, and stability book values sourced from MAIB reports are always **Tier 3** unless independently verified. Desktop assessments must be tagged as assumptions.

---

## 7. T_irr Framework Application

### Rule 7.1 — Mechanism Labels

The T_irr mechanism label must accurately describe the physical progression:

| Label | Use When |
|---|---|
| GRADUAL_DEGRADATION | Environmental conditions progressively worsened, eroding the operational margin over time |
| SUDDEN_ONSET | A rapid environmental event (squall, downdraft, rogue wave) exceeded the margin instantaneously |
| STABLE_ENVIRONMENT | Environmental conditions were stable or improving; the hazard was entirely operational |
| THRESHOLD_BREACH | Conditions crossed a specific vessel threshold (e.g., Wolfson limit, self-shooting limit) |

### Rule 7.2 — Baseline vs Event Analysis

When T_irr is computed at the ERA5 synoptic baseline for a case involving a mesoscale or transient event, the report must explicitly state that the analysis provides a **lower bound** — the margin at the baseline conditions. If the margin is thin at baseline, it is necessarily thinner or non-existent at the actual event intensity.

### Rule 7.3 — Negative Findings

When T_irr shows Regime 1 (Safe) with full decision budget, the report should frame this as a negative finding: "Environmental conditions did not constrain the decision window. The full operational decision budget was available at the time of the incident."

---

## 8. ERA5 Resolution and Calibration

ERA5 is a gridded reanalysis product that estimates the synoptic-scale atmospheric and ocean-wave environment. It is not a point measurement. ERA5 values represent conditions averaged over a grid cell of approximately 31 km horizontally and 1 hour temporally. Localised phenomena — including convective gust fronts, harbour-scale wind acceleration, topographic channelling effects, tidal-current-wave interaction, and short-lived squalls — may occur between grid cells or between hourly timestamps and will not be resolved by ERA5. Where a case involves such phenomena, the reconstruction must state this limitation explicitly and present ERA5 as the synoptic baseline, not the peak or localised condition.

### Rule 8.1 — Resolution Disclosure

Every reconstruction must state ERA5 horizontal resolution (~31 km) and temporal resolution (1 hour) in the methodology section and in the limitations section.

### Rule 8.2 — Enclosed Waters

For estuarine, harbour, or fjord locations where ERA5 wave data is land-masked, the report must:
- State that wave data is unavailable and explain why
- Cite any MAIB wave/sea-state observation as Tier 3
- If a compatibility shim is used, state that it does not enter the Tier 1 evidence chain

### Rule 8.3 — Gust Factor Review

If the ERA5 gust-to-sustained ratio exceeds 2.0, the report should note this is above the typical open-ocean range and may reflect ERA5 parameterisation in sheltered or convectively unstable conditions.

---

## 9. Anonymisation Standard

### Rule 9.1 — Systematic Anonymisation

All published reconstructions are anonymised. The following are removed:
- Vessel name
- Owner/operator name
- Individual names
- Port names (replaced with geographic descriptions)
- Specific dates in cover metadata (replaced with "Winter storm period," "Summer daytime operations," etc.)

### Rule 9.2 — Vessel Identification

Vessel particulars are rounded: LOA to nearest metre with "~" prefix, GT to nearest hundred/thousand, year of build to decade. Flag state stated as "Foreign-registered" or "UK."

### Rule 9.3 — Identifiability Acknowledgement

Anonymisation is applied to avoid gratuitous naming of vessels or individuals in analytical publications. It does not prevent identification by maritime professionals familiar with the underlying incidents. The purpose is analytical neutrality — presenting environmental data without unnecessary personalisation — not concealment of public-record information.

---

## 10. Report Structure (Minimum Sections)

Every flagship reconstruction must include:

1. Executive Summary
2. Incident Overview (with Vessel Profile card)
3. Environmental Timeline (with ERA5 data at each extraction point)
4. Narrative Weather Description (MAIB-stated conditions)
5. Environmental Reconstruction (comparison table: MAIB vs ERA5)
6. Decision-Time Environment (chronological timeline with decision gates)
7. Environmental Profile (verified bar chart)
8. T_irr / Decision Window Assessment (where applicable)
9. Risk Analysis (with quantified score)
10. Key Analytical Finding
11. Evidence Integrity (hash chain)
12. Methodology
13. Limitations and Caveats
14. Closing Statement
15. Evidence Manifest (appendix)

---

## 11. Evidence Chain Requirements

### Rule 11.1 — Minimum Sealing

Every reconstruction must include:
- ERA5 atmospheric source seal (SHA-256)
- ERA5 wave source seal (SHA-256) — or explicit N/A with reason
- Unit Gate configuration hash
- Combined evidence hash
- Blockchain timestamp (Polygon network)

### Rule 11.2 — Artifact Count

Minimum 20 artifacts per reconstruction. Each raw extraction, gated value set, prediction, and analytical output must be individually hashed and listed in the evidence manifest.

---

## 12. Audit and Verification

### Rule 12.1 — Pre-Publication Review

Before publication, every reconstruction must be reviewed against this protocol using the compliance checklist below. All mandatory items must pass before publication.

**Pre-Publication Compliance Checklist:**

| # | Check | Rule | Mandatory |
|---|---|---|---|
| 1 | Extraction window covers first identified decision point | §1.1 | Yes |
| 2 | Minimum 4 extraction timestamps at standard ERA5 hours | §1.1, §1.2 | Yes |
| 3 | Every MAIB-stated environmental parameter appears in reconstruction | §2.2 | Yes |
| 4 | All ERA5 vs MAIB divergences explicitly flagged with both values | §2.1 | Yes |
| 5 | Threshold tags factually match the data (no mislabelling) | §3.1 | Yes |
| 6 | Duration/exposure claims sourced from MAIB or labelled as estimates | §4.1, §4.2 | Yes |
| 7 | Foreseeability claims grounded in forecast evidence or MAIB statement | §5.1 | Yes |
| 8 | All values classified as Tier 1, 2, or 3 | §6.1 | Yes |
| 9 | T_irr mechanism label matches the physical progression | §7.1 | Yes |
| 10 | ERA5 resolution stated in methodology and limitations sections | §8.1 | Yes |
| 11 | Enclosed-water wave data limitation disclosed if applicable | §8.2 | Conditional |
| 12 | Wolfson thresholds presented as ranges (both limits) | §3.2 | Conditional |
| 13 | Uncertainty caveat included for near-threshold comparisons | §3.3 | Conditional |
| 14 | All minimum sections present (§10 list) | §10 | Yes |
| 15 | ERA5 source seals, Unit Gate hash, and combined hash present | §11.1 | Yes |
| 16 | Minimum 20 evidence artifacts in manifest | §11.2 | Yes |
| 17 | No fault, liability, or blame language anywhere in report | Scope | Yes |
| 18 | Protocol version stated in report metadata | §12.3 | Yes |

### Rule 12.2 — Post-Publication Audit

Published reconstructions are not amended. Findings from post-publication audits are incorporated into this protocol for future reports. The methodology paper provides the authoritative context for interpreting earlier reports.

### Rule 12.3 — Protocol Versioning

This protocol is versioned. Changes are documented with effective dates. All reconstructions state which protocol version they were produced under.

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| 1.0 | March 2026 | Implicit methodology. Documented in Flagship Reconstruction Manual v1.0. |
| 1.1 | April 2026 | Codified from five-report forensic audit. Added: scope statement and non-liability declaration; extraction window discipline anchored to first operational decision with 6-hour default (§1); source discrepancy handling with bounds approach (§2); threshold language rules (§3); duration/exposure claim rules (§4); foreseeability standards (§5); three-tier data classification (§6); T_irr mechanism labels including SUDDEN_ONSET and STABLE_ENVIRONMENT (§7); ERA5 resolution and known-limitation framing (§8); anonymisation standard with intent clarification (§9); minimum report structure (§10); evidence chain requirements (§11); audit procedures with 18-point pre-publication compliance checklist (§12). |

---

**FishIntel Global** — Maritime Foreseeability Intelligence  
Reconstruction Protocol v1.1 — April 2026  
© FishIntel Global (FIG LTD)
