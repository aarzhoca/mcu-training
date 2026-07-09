# 8-Week Syllabus

Time budget: 5–8 hours/week. Each week ends with a working, demo-able deliverable.

## Week 1 — Toolchain & First Blink
- Install VS Code + Nuvoton NuMicro extension; clone board BSP
- Build, flash, and debug a BSP sample; then create your own project
- Explore board schematic and pinout
- **Deliverable:** LED blink from a self-built project; single-step in the debugger and inspect registers

## Week 2 — GPIO & Buttons
- GPIO input/output modes, pull-ups, software debouncing
- Map digital-logic knowledge (counters, FSMs) to firmware state machines
- **Deliverable:** Button-controlled LED patterns driven by a small software state machine

## Week 3 — UART & printf Debugging
- UART config, baud rate, polled TX/RX; retarget printf
- Serial terminal usage (PuTTY / VS Code serial monitor)
- **Deliverable:** UART echo + simple text command parser (e.g., "LED ON")

## Week 4 — Timers & PWM
- Hardware timers, periodic interrupts vs. delay loops
- PWM generation, frequency vs. duty cycle
- **Deliverable:** LED breathing effect; 1 ms system tick driving a mini scheduler

## Week 5 — Interrupts & Event-Driven Design
- NVIC, ISR rules, `volatile`, shared-data hazards
- Refactor Weeks 2–3 code from polling to interrupt-driven
- **Deliverable:** Interrupt-driven button + UART RX; short write-up: polling vs. interrupts

## Week 6 — ADC & Sensors
- Sampling, resolution, reference voltage; moving-average filtering
- **Deliverable:** Live sensor readings over UART; PWM brightness tracks a potentiometer

## Week 7 — I2C / SPI
- Bus protocols, addressing, datasheet-driven driver writing
- Verify traffic with a logic analyzer
- **Deliverable:** Working driver for an I2C or SPI device (temp sensor or display)

## Week 8 — Capstone
- Integrate 3+ peripherals into one application with documented architecture
- **Deliverable:** Demo + README with block diagram and lessons learned

## Stretch (post-program)
- FreeRTOS tasks/queues/semaphores; low-power modes; edge AI on M55M1-class parts
