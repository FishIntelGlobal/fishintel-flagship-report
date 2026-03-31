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
   ```
   python -c "import hashlib; f=open('FILENAME.pdf','rb').read(); print(hashlib.sha3_256(f).hexdigest())"
   ```
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

---

## Disclaimer

These reports are anonymised public versions. They do not name vessels, crew, operators, or investigating bodies. They do not attribute fault or negligence to any individual. The reconstructions evaluate environmental evidence, not the decisions of specific persons.

Source incident data is Crown copyright (MAIB), used in accordance with published reproduction terms.

Environmental reconstruction methodology and system: © FishIntel Global (FIG LTD).

---

## Contact

**FishIntel Global**  
Maritime Foreseeability Intelligence  
[www.fishintelglobal.com](https://www.fishintelglobal.com)
