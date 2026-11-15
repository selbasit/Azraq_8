# Azraq Final Integrated Fluid Model

Unified four-well Streamlit model for **Azraq K-1, K-2, K-3 and K-5**.

## Final scope
- CSV/LAS well-log ingestion and mnemonic harmonization.
- Built-in four-well formation framework with optional replacement tops CSV.
- Vsh, PHIT, PHIE, Sw, Sh, BVW, reservoir and net-pay screening.
- Archie, Simandoux, Indonesian and Dual-Water screening saturation options.
- TG + C1-C5 mud-gas ratios: Wetness, Balance, Character, C1/C2, C1/C3 and C3+.
- Haworth/Pixler-style fluid screening with fluorescence-aware confidence.
- Field-wide evidence calibration using available DST/API, pressure, MDT fluid samples and cores.
- K-means electrofacies, Isolation Forest anomaly QC and Rw sensitivity.
- Four-well correlation and unified field/formation synthesis.
- Downloadable interpreted well, gas-fluid, calibration and field-summary CSVs.

## Included wells
- Azraq K-1: SLAM-2 + SLAM-3 and Shows Summary.
- Azraq K-2: PEX and Shows Summary.
- Azraq K-3: SLAM and Shows Summary.
- Azraq K-5: merged PEX-HRLA-HNGS-DSI-PPC-SP LAS and Shows Summary.

## Evidence hierarchy
**Direct fluid / DST / PVT evidence > calibrated pressure & mobility > core/CST > calibrated petrophysics > mud-gas ratios & fluorescence > raw log-response screening.**

## Important interpretation limits
- HC response is a log-response screen; it does not prove oil type, viscosity, producibility or commerciality.
- TG is used mainly for gas-signal strength/confidence. Relative C1-C5 composition is used for fluid-character screening.
- “Heavier-oil tendency” is not a measured heavy-oil classification. API gravity, viscosity/PVT or direct fluid data are required.
- Final structural/contact work should use standardized TVDSS and deviation surveys.

## Run
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
```

The package is intended as a calibrated **screening and decision-support platform**, not a reserves-booking or production-forecast model.
