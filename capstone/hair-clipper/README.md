# Smart Hair Clipper Controller

Rebuild the electronics of a cordless clipper around the NuMaker MCU.

## Feature roadmap
1. **P0 — Motor PWM control:** 3 speed settings via button, soft-start ramp
2. **P0 — Battery gauge:** ADC divider on Li-ion cell, 3-level LED indicator, low-battery cutoff FSM
3. **P1 — Auto torque boost:** ADC current sense; raise duty when load current spikes
4. **P1 — Stall detection:** sustained overcurrent → shutdown + fault LED
5. **P2 — UART telemetry:** runtime, speed, current logging

## Safety notes
- Work at battery voltage only (3.7–5V); never mains
- Flyback diode across the motor; MOSFET driver between MCU and motor
- Fuse or polyfuse in series with the battery
