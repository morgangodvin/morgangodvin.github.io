# THC / FTIR Quantification (DCC Grant Opportunity)

Durable version of the **THC potency testing briefing** (compiled 2026-07-08). Feeds the
[California cannabis DCC grant](../projects/california-cannabis-dcc-grant.md).

## The idea in one line

Use DCLA's existing **Bruker ALPHA II FTIR** (currently qualitative street-drug ID only) to
establish **validated quantitative THC testing**: scan every sample in-house, send a subset to an
accredited HPLC lab for a reference number, train a **PLS regression model**, and progressively
cut reliance on outsourced testing.

## Why it's novel (fundable framing)

- **No US** harm-reduction or academic drug-checking program does chemometric (regression-based)
  FTIR quantification for **any** substance — confirmed standing gap.
- **No one anywhere** has a published validated FTIR quantification protocol for **cannabis THC**.
- The technique itself is proven for other substances → low methodological risk, high novelty.

## Precedent (the technique exists elsewhere)

- **Netherlands / DIMS** — FTIR concentration estimation operationally since **2016** (MDMA,
  amphetamine, ketamine); error margins MDMA ±10%, amphetamine ±15%. No formal validation paper.
- **Belgium / NICC** — published the chemometric method (Deconinck et al. 2019, Talanta; PLS-DA
  96% correct).
- **Canada / UVic** — published **PLS regression FTIR model for fentanyl** in a live service
  (Gozdzialski, Wallace, Hore 2023, PMC10039693).
- **US** — confirmed gap: UNC, RI FTIR pilot, CFSRE all keep FTIR qualitative-only.

## The chemistry that makes it sound

- Reference method must be **HPLC, not GC** — GC's hot injector decarboxylates THCA→THC during the
  run (GC-MS recovered only 47–66% of the acids vs LC-MS). ATR-FTIR doesn't heat the sample.
- Target: **Total THC (%) = (THCA % × 0.877) + Δ9-THC %**.
- THCA vs THC **is** distinguishable by FTIR (1288 cm⁻¹ carboxyl band disappears on conversion;
  quantitation window ~1250–952 cm⁻¹). Geskovski 2021: THC R²=0.99, RMSEP 2.32%.

## Build runway (calibration size tracks matrix complexity, not instrument)

- Simple matrices (meth powder, MDMA tablets): usable at **96–500** paired samples.
- Cannabis flower (messier — multiple cannabinoids, terpenes, moisture, cultivar): **700–900+**.
- Reference-testing cost ~$50–100/sample → ~$21k–90k over the grant life, but **dual-purpose**
  (each is both a compliance number and a training point).
- Software: Bruker **OPUS QUANT2** is built for this; free alternatives R `pls`/`mdatools` or
  scikit-learn.
- Hardware/software gap: **none** — ALPHA II specs clear the bar. The only gap is the reference
  dataset + a chemometrician.

## Landmines
- **Sampling/homogenization matters twice as much** — bad sampling teaches the model wrong. Grind
  <1mm before both the scan and the HPLC split (ASTM D8493-23 / CA DCC 4 CCR §15714(a)).
- **Moisture basis** — pick one and hold it constant (states disagree: Ohio bans dry-weight
  correction, Vermont requires it).
- **CA lab quality** — CA went 37→27 labs under enforcement; several cited for THC inflation. A
  biased reference lab bakes bias into every future FTIR prediction. Pick a clean-record lab; do
  occasional cross-lab validation. DCLA (nonprofit, no inflation incentive) is well positioned.
- No literature validates FTIR quantification below ~5–10% w/w — expect a low-end floor where
  outsourced confirmation is always needed.

Full sourced briefing with all citations is the artifact `thc-potency-testing-briefing.md`.
