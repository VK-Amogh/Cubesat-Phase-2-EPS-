CubeSat EPS Simulation (CircuitJS)

This repository contains a simplified Electrical Power System (EPS) model for a CubeSat, implemented for the CircuitJS simulator. It demonstrates a solar source (PWL), battery, OBC/ADCS always-on loads, and switched Payload and TT&C loads. The orbit is scaled for fast simulation: 9 s total (6 s sunlight, 3 s eclipse).

## Contents
- `circuitjs/cube_eps.json` — ready-to-import CircuitJS schematic JSON (wired and parameterized).
- `report/EPS_Report.md` — technical report describing design, assumptions, results.
- `docs/how_to_run.md` — step-by-step run instructions and expected waveforms.
- `src/analyze_results.py` — optional helper to parse exported CSV from CircuitJS (if you export traces).

## Quickstart
1. Open CircuitJS (https://www.falstad.com/circuit/ or your local instance).
2. Import `circuitjs/cube_eps.json` (File → Import).
3. Run the simulation and open the Scope for `V(bus)` and `I(battery)` traces.
4. Expected behavior: bus ≈ 7.4 V during sun (0–6 s), slight droop during eclipse (6–9 s). Battery charges slightly in sun and discharges in eclipse. Payload active only in sun; TT&C bursts are short pulses.

## Notes
- The schematic uses a VCCS with a PWL function for a 9 s orbit: `pwl(t,0,0,6,0.81081,6,0.81081,9,0)`.
- Switch control pulses and exact component values are documented in `circuitjs/README.md` and `docs/how_to_run.md`.
