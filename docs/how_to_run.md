# How to run the CubeSat EPS simulation (CircuitJS)

## Import
1. Open CircuitJS (Falstad) at https://www.falstad.com/circuit/ .
2. File → Import → paste the contents of `circuitjs/cube_eps.json` (or load the file if your instance supports it).

## What to probe
- Add Scope traces for:
  - `V(bus)` (voltage of the main positive bus node w.r.t ground)
  - `I(battery)` (current through the battery; positive = charging)
  - `V(payload)` (node across payload resistor)
  - `V(ttc)` (node across TT&C resistor)

## Simulation settings & strings (exact)
- Solar (VCCS function, VCCS property `#inputs = 0`):
