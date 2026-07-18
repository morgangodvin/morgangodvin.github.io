# Fentanyl Epidemiology — Timing of the Takeover

Durable version of two interactive dashboards built from CDC WONDER data:
1. **Fentanyl's transition speed: first signal → domination**
2. **Fentanyl onset → peak overdose mortality**

## Data & method (shared)

- **Source:** CDC WONDER Multiple Cause of Death — final 1999–2020 spliced with provisional
  2021–2025 (pulled **10 Jul 2026**). 2025 is provisional and will revise upward.
- Fentanyl = ICD-10 **T40.4** (synthetic opioids). Opioid denominator = MCD any of
  T40.0/.1/.2/.3/.4/.6.
- Two selectable denominators: fentanyl as % of **opioid** OD deaths, or of **all-drug** OD deaths.
- "Sustained" crossing = first year at/above a threshold that is still at/above it the next year
  (last year exempt).
- **IMF-era option (≥2013)** filters out pre-2013 pharmaceutical-fentanyl blips (WV/NH/VT) so they
  don't antedate the signal.
- Pre-2013 pharmaceutical background: 95th percentile = 26.8% (opioid denom), 15.6% (all-drug).
  Baselines are set above this.
- All 50 states + DC (51 units). Medians reported (robust to outliers).

## Dashboard 1 — Transition speed (first signal → domination)

For each state, the years between fentanyl's **first signal** (a low share, baseline slider) and
its **domination** (a high share). Measures the *speed* of takeover, not its timing.

- Interactive: baseline slider 10–40%, domination slider 50–90%, color by region / Mississippi
  side / speed, sort by cascade / speed / domination year.
- Output structure: per-state timeline bars; states that showed the signal but never dominated are
  drawn as dotted bars.
- Comparison panel: pin states to compare fentanyl-share curves with signal (●) and domination (◆)
  markers.

## Dashboard 2 — Onset → peak overdose mortality

For each state, the year fentanyl first crossed a chosen share (**onset**) and the years from
there to that state's **peak overdose-death year**.

- Peak = year of maximum death count for the chosen denominator (opioid OD in opioid mode, all-drug
  in all-drug mode).
- **Lag = peak − onset.** Negative lag = the death toll peaked *before* fentanyl reached that share
  (flagged in red).
- Same controls; summary boxes give median lag overall, by census region, and by East/West of the
  Mississippi.

## Why this matters
Both tools frame the same policy point: fentanyl's takeover was fast and cascaded geographically
(broadly East → West of the Mississippi), and mortality peaks track onset with a measurable lag —
useful for anticipating where a supply is on the curve.

## Reuse
The state-year arrays (`t` = fentanyl deaths, `o` = opioid OD deaths, `a` = all-drug OD deaths, per
year 1999–2025) are embedded in both artifacts and can be re-extracted for new analyses. Both are
owned artifacts on claude.ai/code.
