# FishIntel Global — Environmental Reconstruction Report

## Decision-Time Foreseeability Intelligence for Maritime Incidents

This repository contains the first publicly released FishIntel environmental reconstruction report. The report demonstrates how quantified environmental reconstruction reveals what was objectively knowable before a critical maritime operational decision was made.

---

## Case Summary

A foreign-registered bulk carrier, anchored in ballast at a UK coastal anchorage, dragged its anchor during a severe winter storm and grounded on a public beach. The vessel was successfully refloated on the next high water. No injuries, no pollution.

FishIntel reconstructed the environmental conditions at the anchorage position across a three-point time window using ECMWF ERA5 atmospheric reanalysis data.

**Key finding:** The vessel was in a maximum-risk (100%) anchoring regime across the entire incident window. The dominant forcing was heavy swell propagating into the anchorage from the open ocean, combined with severe gust loading — not sustained storm-force local wind alone. The conventional Beaufort force 9–10 description in the narrative account conflated two distinct physical mechanisms: local wind and remotely generated swell.

---

## Report

**[FishIntel_Environmental_Reconstruction_v1_0.pdf](reports/FishIntel_Environmental_Reconstruction_v1_0.pdf)** — The full reconstruction report (PDF).

**[FishIntel_Flagship_Report_CANONICAL_v2.html](reports/FishIntel_Flagship_Report_CANONICAL_v2.html)** — The interactive HTML version.

---

## Blockchain Verification

This report is timestamped on the Polygon blockchain. The document hash was recorded immutably on-chain, proving the report existed in its current form at the time of the transaction.

| Field | Value |
|---|---|
| **Document Hash (SHA3-256)** | `f7b75378eb175e5fa756628d4d2c64134b5971308e1f81aff846cdf2308135b5` |
| **Polygon Transaction** | [`0x6748afca99fa221299cbe524b1849a0f91834932db36db3735df3ffeb9c3f9b0`](https://polygonscan.com/tx/0x6748afca99fa221299cbe524b1849a0f91834932db36db3735df3ffeb9c3f9b0) |
| **Verification Wallet** | `0x352C97a8e550942186f1A497e532027CB4583605` |
| **Timestamp** | 31 March 2026 |

**To verify:** Download the PDF, compute its SHA3-256 hash, and compare against the hash recorded in the Polygon transaction data field. They must match exactly.

---

## Methodology

FishIntel reconstructs the environmental conditions surrounding maritime incidents using ECMWF ERA5 atmospheric reanalysis data — the same dataset relied upon by meteorological agencies, climate researchers, and aviation safety authorities worldwide.

The reconstruction pipeline extracts environmental variables at the precise coordinates and time window of each incident. All values pass through a unit-gated validation layer that enforces explicit conversion factors and plausibility bounds using Decimal arithmetic. The pipeline is deterministic: identical inputs always produce identical outputs.

---

## Pipeline Integrity

| Component | Version |
|---|---|
| ERA5 Processor | v5.3.0 |
| Reconstruction Runner | v2.2.0 |
| Unit Gate Config Hash | `989aadf7b9b1a4acef8606e162015337e75a8ce5fcb4edfb1e0d79f4d59513aa` |
| Output Format | `era5_raw_v1` |

---

## Disclaimer

This report is an anonymised public version. It does not name the vessel, crew, operator, or investigating body. It does not attribute fault or negligence to any individual. The reconstruction evaluates environmental evidence, not the decisions of specific persons.

Source incident data is Crown copyright, used in accordance with published reproduction terms.

Environmental reconstruction methodology and system: © FishIntel Global (FIG LTD).

---

## Contact

**FishIntel Global**
Maritime Foreseeability Intelligence

[www.fishintelglobal.com](https://www.fishintelglobal.com)
