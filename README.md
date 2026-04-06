# FishIntel Global — Environmental Reconstruction Reports

**Publisher:** FishIntel Global (FIG LTD)  
**Methodology:** ERA5 atmospheric reanalysis → deterministic reconstruction pipeline  
**Verification:** SHA3-256 document hashing → Polygon blockchain timestamping

---

## Published Reports

### Flagship 1 — Anchorage Failure During Forecast Storm Conditions

Decision-time environmental reconstruction of a bulk carrier grounding following anchor drag during a severe winter storm at a UK coastal anchorage.

**Key finding:** ERA5 reconstruction separates local wind forcing from remotely generated swell, revealing that the conventional Beaufort Force 9–10 classification conflated two distinct physical mechanisms. The hazardous regime was established more than 90 minutes before the anchor began to drag.

- **HTML:** [FIG_Flagship_Report_v1.0.html](FIG_Flagship_Report_v1.0.html)
- **PDF:** [FishIntel_Environmental_Reconstruction_v1_0.pdf](FishIntel_Environmental_Reconstruction_v1_0.pdf)
- **Reference:** FIG-2025-001
- **Risk classification:** HIGH (100%)

### Flagship 2 — Routine Environmental Conditions at the Stability Limit

Decision-time environmental reconstruction of a fishing vessel capsize during single-handed trawling operations in the English Channel.

**Key finding:** ERA5 reconstruction confirms that the vessel capsized in conditions classified as LOW–MODERATE risk (36.7–41.1%). Sustained wind was 15.3–16.7 knots (Force 4), significant wave height was 0.82–0.88 m, and visibility was good. The vessel's stability margin placed it only 35 mm above the Wolfson danger-of-capsize zone. The environmental conditions were foreseeable and matched the published forecast. The information required to calculate the vessel's vulnerability existed but had not been computed.

- **HTML:** [FishIntel_Environmental_Reconstruction_v2_0.html](FishIntel_Environmental_Reconstruction_v2_0.html)
- **Reference:** FIG-2026-002
- **Risk classification:** LOW–MODERATE (36.7–41.1%)

---

## Blockchain Evidence Chain

Every published report is hashed (SHA3-256) and timestamped on the Polygon blockchain. This creates an immutable, publicly verifiable record that the document existed in its exact form at the time of the transaction.

### Flagship 1

| Field | Value |
|---|---|
| **PDF** | `FishIntel_Environmental_Reconstruction_v1_0.pdf` |
| **SHA3-256** | `dd29853df2483532cc76b42f0c8c2d75bcd9e62e5fb33a783cb4ba96223d73c0` |
| **Polygon TX** | [`0x4376ab79a86067db85621207bed63400abd245fc84056c3e832662d536a514ff`](https://polygonscan.com/tx/0x4376ab79a86067db85621207bed63400abd245fc84056c3e832662d536a514ff) |
| **Wallet** | `0x352C97a8e550942186f1A497e532027CB4583605` |

### Flagship 2

| Field | Value |
|---|---|
| **PDF** | `FishIntel_Environmental_Reconstruction_v2_0.pdf` |
| **SHA3-256** | `74e5cbf3e2b6270ca3cb4ef46637a10a1e6bfe60ba230344547a378317644588` |
| **Polygon TX** | [`0xc8c2e824ed0100935f87c6e7bf5dd176363c9e1a0a0f64dadd2cf929d9157156`](https://polygonscan.com/tx/0xc8c2e824ed0100935f87c6e7bf5dd176363c9e1a0a0f64dadd2cf929d9157156) |
| **Wallet** | `0x352C97a8e550942186f1A497e532027CB4583605` |

---

## How to Verify

Any party can independently verify the integrity of a published report:

1. Download the PDF from this repository
2. Compute its SHA3-256 hash:
3. Compare the hash to the value recorded in the Polygon transaction
4. View the transaction on [PolygonScan](https://polygonscan.com) to confirm the timestamp and data

If the hashes match, the document has not been modified since the blockchain timestamp was created.

---

## Pipeline Integrity

| Component | Version |
|---|---|
| ERA5 Processor | v5.3.0 |
| Reconstruction Runner | v2.1.0 |
| Output Format | `era5_raw_v1` |

The pipeline is deterministic: identical inputs always produce identical outputs. All values pass through explicit unit conversion (m/s → knots, Pa → hPa, K → °C) with no manual adjustments, interpolations, or subjective corrections.

ERA5 data is freely available from the [Copernicus Climate Data Store](https://cds.climate.copernicus.eu) and independently verifiable by any party.

### FIG-FLAGSHIP-003 — Sailing Yacht Capsize, Sicily, August 2024
- **Report:** [Environmental Reconstruction v3.0](FishIntel_Environmental_Reconstruction_v3_0.html)
- **Incident:** Capsize of 56m sailing yacht during mesoscale convective downdraft — 7 fatalities
- **SHA3-256:** `7ca646682fd66fe57833d71a599c3794acc927c35044a1f4f83b4d0d4acf0932`
- **Blockchain TX:** [`0xcebf73f3...`](https://polygonscan.com/tx/0xcebf73f3c0764377ebd7760aa2dd459f0f43823b931dc36dd637bb6bcacc867a)
- **Wallet:** `0x352C97a8e550942186f1A497e532027CB4583605`

---

## Disclaimer

These reports are anonymised public versions. They do not name vessels, crew, operators, or investigating bodies. They do not attribute fault or negligence to any individual. The reconstructions evaluate environmental evidence, not the decisions of specific persons.

Source incident data is Crown copyright (MAIB), used in accordance with published reproduction terms.

Environmental reconstruction methodology and system: © FishIntel Global (FIG LTD).

---
---

### FIG-FLAGSHIP004 — Environmental Reconstruction — Fatal Man Overboard

- **Incident:** Fatal man overboard during creel shooting operations, 5 February 2018
- **Vessel:** UK creel fishing vessel — 18.2m
- **Location:** Approximately 16nm north-west of Cape Wrath, Scotland
- **Scope:** Environmental reconstruction only (T_irr not applied — crew-level hazard)
- **Key finding:** ERA5 sustained wind 24.4–25.7 kt (Force 6) across full 4-hour window; MAIB-stated 35 kt aligns with ERA5 gust (36.1 kt), not sustained wind
- **HTML:** [FishIntel_Environmental_Reconstruction_NorthStar_v1_0.html](FishIntel_Environmental_Reconstruction_NorthStar_v1_0.html)
- **PDF:** [FishIntel_Environmental_Reconstruction_NorthStar_v1_0.pdf](FishIntel_Environmental_Reconstruction_NorthStar_v1_0.pdf)
- **Document hash (SHA3-256):** `109b9d9f4e4812eea1bc7c8e991f08abda9c7c7c0b2a954adc59e4e0195ffda9`
- **Polygon TX:** [`0x498ae0b6...`](https://polygonscan.com/tx/0x498ae0b67917a0d883ebb8552f0d403c736038e211fc7ca0672d4c037cf2794a)
- Wallet: `0x352C97a8e550942186f1A497e532027CB4583605`
  ---

### FIG-FLAGSHIP005 — Environmental Reconstruction — Tug Capsize During Ship Assist Towage

- **Incident:** Capsize of tug during ship assist towage, 24 February 2023
- **Vessel:** Twin screw workboat / tug — Very Serious Marine Casualty (2 fatalities)
- **Location:** Navigational channel off Greenock, Scotland
- **Scope:** Atmospheric-only reconstruction (ERA5 wave data land-masked at location). T_irr decision-window analysis.
- **Key finding:** ERA5 confirms operationally benign conditions throughout. Wind 7.3 kt sustained at decision frame, declining to 6.1 kt. T_irr: REGIME_1_SAFE — full environmental decision budget intact. No environmental forcing capable of contributing to the capsize was detected.
- **HTML:** [FishIntel Environmental Reconstruction FLAGSHIP005 v1 0.html](FishIntel_Environmental_Reconstruction_FLAGSHIP005_v1_0.html)
- **PDF:** [FishIntel Environmental Reconstruction FLAGSHIP005 v1 0.pdf](FishIntel_Environmental_Reconstruction_FLAGSHIP005_v1_0.pdf)
- **Document hash (SHA3-256):** `024ec3ce3e50bbadb1aa22c117a2ea0d8aaf8f98e5755235074fedc3506f8cb2`
- **Polygon TX:** [`0xb0b139a7...`](https://polygonscan.com/tx/0xb0b139a7da6b4b338b0f83186826b6363aaa1461e410ec3021ab1117ab67761b)
- **Wallet:** `0x352C97a8e550942186f1A497e532027CB4583605`
  
  ## Contact

**FishIntel Global**  
Maritime Foreseeability Intelligence  
[www.fishintelglobal.com](https://www.fishintelglobal.com)
