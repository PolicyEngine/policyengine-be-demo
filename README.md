# PolicyEngine Belgium — prototype

A static prototype of a PolicyEngine country app for Belgium: CIR 92 reform levers
(art. 131 basic exemption, art. 130 top rate, communal surcharge) computed over the
Microcosm-BE population, with household net-income curves and society-wide impacts.

Every figure is computed by the Axiom rules engine executing statute-grounded
encodings from [rulespec-be](https://github.com/TheAxiomFoundation/rulespec-be),
validated case by case against EUROMOD BE_2025 via
[axiom-oracles](https://github.com/TheAxiomFoundation/axiom-oracles). The
population layer is [Microcosm](https://github.com/PolicyEngine/microcosm)-BE,
calibrated to Chronicle targets (sums of published administrative facts) — see the
[calibration dashboard](https://microcosm.institute/calibration/dashboard/microcosm?country=be).

Reform cells (`data.json`) were computed in July 2026 on the pilot worker slice;
a recompute on Microcosm-BE v0.5 is queued. The page also carries the v0.5
truth/Axiom/EUROMOD aggregate check and two computable-core exhibits beyond
tax-benefit (penal fine décimes, statutory interest).

Static files, no build step:

```bash
python3 -m http.server 4173
```
