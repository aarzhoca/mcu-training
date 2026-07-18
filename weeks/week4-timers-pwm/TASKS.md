# Week 4 — Timers & PWM

**Goal:** Replace delay loops with hardware timing; generate PWM.
**Branch:** `week4/timers-pwm` · **Reading:** M031 TRM — Timer Controller & PWM Generator chapters; BSP samples `TIMER_PeriodicINT`, `PWM_OutputWaveform`

## Tasks
- [ ] **T4.1** Configure a hardware timer for a 1 ms periodic interrupt; maintain a `uint32_t ms_ticks` counter (mark it `volatile` — we'll dig into why in Week 5)
- [ ] **T4.2** Rebuild your Week 2 blink FSM using `ms_ticks` for timing instead of delay loops — the CPU should never busy-wait
- [ ] **T4.3** Configure a PWM channel on the LED pin at 1 kHz; step the duty cycle via UART commands (`PWM 25`, `PWM 50`, `PWM 100`)
- [ ] **T4.4** LED breathing effect: ramp duty 0→100→0 smoothly using the 1 ms tick (no delays). Aim for a ~2 s breath cycle
- [ ] **T4.5** Calculate by hand: for your PWM clock source and prescaler, what period register value gives exactly 1 kHz? Show the math in the notes; verify with the debugger
- [ ] **T4.6** Commit + PR "Week 4 — timers & PWM"

## Acceptance criteria
- Zero blocking delay loops anywhere in the final code
- Breathing effect is smooth (no visible stepping)
- Period/prescaler math written out and matches the register values

## Notes / math / takeaways
