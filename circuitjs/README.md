# CircuitJS schematic for CubeSat EPS

This folder contains `cube_eps.json` — an export you can import into CircuitJS. The file contains:
- Battery (7.4 V + 0.15 Ω)
- Solar Voltage Controlled Current Source using PWL time function (9 s orbit)
- Loads as resistors
- Analog SPST switches with Square wave Source (PULSE) control sources
- scopes

Open circuit and run. Edit pulse timing and the orbital timings as I have taken 9 seconds (6s in the contact of the sun and 3s at eclipse) (insted of 90min for quicker waveform) if you want to simulate different duty cycles.
