# Week 6 — ADC & Sensor Reading

**Goal:** Bring analog signals into the digital world — and filter them.
**Branch:** `week6/adc` · **Hardware:** 10k potentiometer on a breadboard → ADC channel pin (3.3V, GND, wiper). **Reading:** M031 TRM — ADC chapter (resolution, sample time, reference); BSP sample `ADC_SingleMode`

## Tasks
- [ ] **T6.1** Wire the pot (double-check the pin is 3.3V-tolerant analog-capable from the datasheet pin table) and read single conversions; print raw counts over UART
- [ ] **T6.2** Convert counts to millivolts in fixed-point (no floats). What does 1 LSB equal in mV for a 12-bit ADC at 3.3 V? Show in notes
- [ ] **T6.3** Sample at 100 Hz using your 1 ms tick; stream `raw, mV` as CSV over UART; capture 10 s and plot it (Excel/Python — your choice)
- [ ] **T6.4** Implement a moving-average filter (window 8 or 16 — use a power of 2 and explain why). Stream raw vs. filtered side by side; plot both and observe the noise reduction — connect this to your analog filters coursework
- [ ] **T6.5** Close the loop: filtered pot value sets LED PWM duty (knob = dimmer). This is your first sensor→processing→actuator pipeline
- [ ] **T6.6** Commit + PR "Week 6 — ADC pipeline". Include one plot image

## Acceptance criteria
- Fixed-point mV conversion correct (spot-check with a multimeter if available)
- Plot committed showing raw vs. filtered
- Dimmer responds smoothly with no jitter at rest

## Notes / LSB math / takeaways
