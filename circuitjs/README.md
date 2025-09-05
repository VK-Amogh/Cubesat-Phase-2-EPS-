# CircuitJS schematic for CubeSat EPS

This folder contains `cube_eps.json` — an export you can import into CircuitJS. The file contains:
- Battery (7.4 V + 0.15 Ω)
- Solar Voltage Controlled Current Source using PWL time function (9 s orbit)
- Loads as resistors
- Analog SPST switches with Square wave Source (PULSE) control sources
- scopes
- Battery: 7.4 V, internal 0.15 Ω.

Resistors:
- OBC: 55
- ADCS: 110
- Payload: 15.534751773049646
- TT&C: 18.253333333333334
- Analog SPST Switch settings:
- Ron: 0.01
- Roff: 1e9
- Threshold (Vt): 2.5
- Pulldown: checked
- Normally closed: unchecked
- TT&C: Square wave params: Max=5, Offset=0, Frequency=1/9 ≈ 0.111111 Hz, Duty=5%
- Payload: Square wave params: Max=5, Offset=0, Frequency=1/9 ≈ 0.111111 Hz, Duty=66.7%

Max=5, Offset=0, Frequency=1/9 ≈ 0.111111 Hz, Duty=66.7%

Open circuit and run. Edit pulse timing and the orbital timings as I have taken 9 seconds (6s in the contact of the sun and 3s at eclipse) (insted of 90min for quicker waveform) if you want to simulate different duty cycles.
