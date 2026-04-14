# FishIntel Global — Environmental Reconstruction Reports

**Publisher:** FishIntel Global (FIG LTD)  
**Methodology:** ERA5 atmospheric reanalysis → deterministic reconstruction pipeline  
**Verification:** SHA3-256 document hashing → Polygon blockchain timestamping  
**Protocol:** [Reconstruction Protocol v1.1](FISHINTEL_RECONSTRUCTION_PROTOCOL_v1_1.md) — published April 2026 following forensic audit of all five flagship reports

---

## Reconstruction Protocol

FishIntel reconstructions are governed by a published methodology standard. Protocol v1.1 was codified following a forensic cross-verification audit of the first five flagship reports, conducted in April 2026.

The protocol defines extraction window discipline, three-tier evidence classification, source discrepancy handling, threshold language rules, T_irr framework application standards, and an 18-point pre-publication compliance checklist.

**Document:** [FISHINTEL_RECONSTRUCTION_PROTOCOL_v1_1.md](FISHINTEL_RECONSTRUCTION_PROTOCOL_v1_1.md)

**Independent Review:** [Independent Review Protocol v1.0](FIG_Independent_Review_Protocol_v1_0.pdf) — every reconstruction independently reviewed before publication
---

## Published Reports

### Flagship 001 — Anchorage Failure During Forecast Storm Conditions

Decision-time environmental reconstruction of a bulk carrier grounding following anchor drag during a severe winter storm at a UK coastal anchorage. 17-section report with T_irr time-to-irreversibility analysis.

**Key finding:** ERA5 reconstruction separates local wind forcing from remotely generated swell, revealing that the conventional Beaufort Force 9–10 classification conflated two distinct physical mechanisms. All three environmental signals exceeded safety thresholds at 21:00 UTC, providing an 8-hour intervention window. T_irr analysis confirms REGIME_1_SAFE with +10.5 minute conservative margin — physical intervention remained possible throughout.

| Field | Value |
|---|---|
| HTML (V2) | FIG_FLAGSHIP001_report_v2.html |
| PDF (V2) | FIG_FLAGSHIP001_report_v2.pdf |
| HTML (V1) | FIG_Flagship_Report_v1.0.html |
| PDF (V1) | FishIntel_Environmental_Reconstruction_v1_0.pdf |
| Reference | FIG-FLAGSHIP-001 |
| Risk classification | EXTREME (100%) |
| T_irr regime | REGIME_1_SAFE (+10.5 min margin) |
| SHA3-256 (V2) | `57cab6da05b531a54d43fb97a25618fa26f978eb6421bade1303e5e89d624fc9` |
| Polygon TX (V2) | [`0x9f90879067b66c1e72d4384a12861a4875e125f5b5933b53aab25b311de0ff1d`](https://polygonscan.com/tx/0x9f90879067b66c1e72d4384a12861a4875e125f5b5933b53aab25b311de0ff1d) |
| SHA3-256 (V1) | `dd29853df2483532cc76b42f0c8c2d75bcd9e62e5fb33a783cb4ba96223d73c0` |
| Polygon TX (V1) | `0x4376ab79a86067db85621207bed63400abd245fc84056c3e832662d536a514ff` |

---

### Flagship 002 — Routine Environmental Conditions at the Stability Limit

Decision-time environmental reconstruction of a fishing vessel capsize during single-handed trawling operations in the English Channel.

**Key finding:** ERA5 confirms the vessel capsized in conditions classified as LOW–MODERATE risk (36.7–41.1%). Sustained wind was 15.3–16.7 knots (Force 4), significant wave height was 0.82–0.88 m. The vessel's stability margin placed it only 35 mm above the Wolfson danger-of-capsize zone. The environmental conditions were foreseeable and matched the published forecast. The information required to calculate the vessel's vulnerability existed but had not been computed.

| Field | Value |
|---|---|
| HTML | FishIntel_Environmental_Reconstruction_v2_0.html |
| PDF | FishIntel_Environmental_Reconstruction_v2_0.pdf |
| Reference | FIG-2026-002 |
| Risk classification | LOW–MODERATE (36.7–41.1%) |
| SHA3-256 | `74e5cbf3e2b6270ca3cb4ef46637a10a1e6bfe60ba230344547a378317644588` |
| Polygon TX | `0xc8c2e824ed0100935f87c6e7bf5dd176363c9e1a0a0f64dadd2cf929d9157156` |

---

### Flagship 003 — Sailing Yacht Capsize During Convective Storm Event

Decision-time environmental reconstruction of a 56 m sailing yacht capsize during a mesoscale convective downdraft off Sicily. Seven fatalities.

**Key finding:** ERA5 synoptic baseline was benign (6.28 kt sustained wind, 0.39 m seas) — all timestamps classified LOW risk. The T_irr framework classifies the operational situation as Regime 2 — Danger, with a conservative margin of only 1.2 minutes. The mesoscale downdraft (>70 kt) was not resolved by ERA5 but was assessed as highly likely in the prevailing conditions by the Met Office post-incident study. The margin between viability and catastrophe was already critically thin at the synoptic baseline.

| Field | Value |
|---|---|
| HTML | FishIntel_Environmental_Reconstruction_v3_0.html |
| PDF | FishIntel_Environmental_Reconstruction_v3.pdf |
| Reference | FIG-FLAGSHIP-003 |
| Risk classification | LOW (25.9–32.1%) — synoptic baseline |
| SHA3-256 | `7ca646682fd66fe57833d71a599c3794acc927c35044a1f4f83b4d0d4acf0932` |
| Polygon TX | `0xcebf73f3c0764377ebd7760aa2dd459f0f43823b931dc36dd637bb6bcacc867a` |

---

### Flagship 004 — Fatal Man Overboard During Creel Shooting Operations

Environmental reconstruction of a fatal man overboard during manual creel shooting operations approximately 16 nm north-west of Cape Wrath, Scotland. T_irr not applied (crew-level hazard).

**Key finding:** ERA5 sustained wind 24.4–25.7 kt (Force 6) across the full 4-hour window. The MAIB-stated 35 kt aligns with the ERA5 gust value (36.1 kt), not the sustained wind. Conditions were synoptic-scale, sustained, and foreseeable. The Force 6 conditions placed the vessel's operational mode within the band associated with manual shooting, where crew were positioned adjacent to running gear without physical barriers.

| Field | Value |
|---|---|
| HTML | FishIntel_Environmental_Reconstruction_NorthStar_v1_0.html |
| PDF | FishIntel_Environmental_Reconstruction_NorthStar_v1_0.pdf |
| Reference | FIG-FLAGSHIP004 |
| Risk classification | HIGH |
| SHA3-256 | `109b9d9f4e4812eea1bc7c8e991f08abda9c7c7c0b2a954adc59e4e0195ffda9` |
| Polygon TX | `0x498ae0b6...` |

---

### Flagship 005 — Tug Capsize During Ship Assist Towage

Atmospheric-only environmental reconstruction of a tug capsize during ship assist towage in a navigational channel off Greenock, Scotland. Two fatalities. ERA5 wave data land-masked at this enclosed estuarine location. T_irr decision-window analysis applied.

**Key finding:** ERA5 confirms operationally benign conditions throughout. Wind 7.3 kt sustained at decision frame, declining to 6.1 kt. T_irr: Regime 1 — Safe. Full environmental decision budget was intact. No environmental forcing capable of contributing to the capsize was detected. The casualty was driven entirely by the operational towing configuration.

| Field | Value |
|---|---|
| HTML | FishIntel_Environmental_Reconstruction_FLAGSHIP005_v1_0.html |
| PDF | FishIntel_Environmental_Reconstruction_FLAGSHIP005_v1_0.pdf |
| Reference | FLAGSHIP005 |
| Risk classification | LOW (17.6%) |
| SHA3-256 | `024ec3ce3e50bbadb1aa22c117a2ea0d8aaf8f98e5755235074fedc3506f8cb2` |
| Polygon TX | `0xb0b139a7...` |

---

## Blockchain Verification

Every published report is hashed (SHA3-256) and timestamped on the Polygon blockchain. This creates an immutable, publicly verifiable record that the document existed in its exact form at the time of the transaction.

**Wallet:** `0x352C97a8e550942186f1A497e532027CB4583605`

### How to Verify

Any party can independently verify the integrity of a published report:

1. Download the PDF from this repository
2. Compute its SHA3-256 hash
3. Compare the hash to the value recorded in the Polygon transaction
4. View the transaction on [PolygonScan](https://polygonscan.com) to confirm the timestamp and data

If the hashes match, the document has not been modified since the blockchain timestamp was created.

---

## Pipeline Integrity

| Component | Version |
|---|---|
| ERA5 Processor | v5.4.3 |
| Reconstruction Runner | v2.4.3 |
| Unit Gate | v1.0.0 |
| T_irr Engine | v1.2.1 |
| Report Renderer | v2.0.0 |
| Output Format | era5_raw_v1 |
| Protocol | v1.1 (April 2026) |

The pipeline is deterministic: identical inputs always produce identical outputs. All values pass through explicit unit conversion (m/s → knots, Pa → hPa, K → °C) with no manual adjustments, interpolations, or subjective corrections.

ERA5 data is freely available from the [Copernicus Climate Data Store](https://cds.climate.copernicus.eu) and independently verifiable by any party.

---

## Disclaimer

These reports are anonymised public versions. They do not name vessels, crew, operators, or investigating bodies in the analytical content. They do not attribute fault or negligence to any individual. The reconstructions quantify environmental evidence, not the decisions of specific persons.

FishIntel reconstructions do not determine liability, fault, or legal responsibility. Their purpose is to establish what environmental conditions were objectively knowable before critical maritime decisions were made.

Source incident data is Crown copyright (MAIB), used in accordance with published reproduction terms.

Environmental reconstruction methodology and system: © FishIntel Global (FIG LTD).

---

## Contact

**FishIntel Global**  
Maritime Foreseeability Intelligence  
www.fishintelglobal.com
