# Week 8+ — Capstone: Smart Hair Clipper Controller

**Goal:** Integrate everything into a real product. See `capstone/hair-clipper/README.md` for the feature roadmap and safety notes — read the safety notes first.
**Branch:** `capstone/main` (feature branches off it as needed)

## Phase 0 — Plan (before writing code)
- [ ] **T8.1** Draw the system block diagram: battery → charger → MCU + motor driver → motor; label every MCU pin used
- [ ] **T8.2** Draw the top-level firmware state machine: `IDLE → RUNNING(speed 1/2/3) → BOOST → FAULT → LOW_BATT`; get mentor sign-off on both diagrams before proceeding

## Phase 1 — Motor control (Week 4 skills)
- [ ] **T8.3** PWM motor drive through the MOSFET board (bench PSU or battery — never USB power for the motor); 3 speeds via button; soft-start ramp (~300 ms)

## Phase 2 — Battery gauge (Week 6 skills)
- [ ] **T8.4** ADC divider on the cell voltage; map voltage → 3-level indicator; low-battery warning and cutoff states in the FSM

## Phase 3 — Auto torque boost (Weeks 5–7 skills)
- [ ] **T8.5** Current sensing via INA219 (I2C — reuse your Week 7 driver pattern) or shunt+ADC; log idle vs. loaded current to pick a boost threshold
- [ ] **T8.6** Boost logic: sustained current above threshold → raise duty; drop back after load clears (add hysteresis so it doesn't oscillate)
- [ ] **T8.7** Stall protection: current above hard limit for >500 ms → `FAULT`, motor off, fault LED

## Phase 4 — Polish & demo
- [ ] **T8.8** UART telemetry: 1 Hz line of `state, duty, mV_batt, mA_motor`
- [ ] **T8.9** Final README in `capstone/hair-clipper/`: block diagram, state diagram, what worked, what didn't, what you'd do differently
- [ ] **T8.10** Demo day: live demo + 10-minute walkthrough of the architecture

## Acceptance criteria
- All P0 features working; boost demonstrated with a real load
- Clean modular code (motor.c, battery.c, current.c, cli.c)
- README tells the story well enough that a stranger could rebuild it
