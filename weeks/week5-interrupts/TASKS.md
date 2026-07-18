# Week 5 — Interrupts & Event-Driven Design

**Goal:** Understand NVIC, ISR discipline, and shared-data hazards.
**Branch:** `week5/interrupts` · **Reading:** M031 TRM — NVIC/Interrupt sections; Cortex-M0 Generic User Guide (exception model); BSP sample `GPIO_INT`, `UART_TxRxFunction` (IRQ mode)

## Tasks
- [ ] **T5.1** Convert the Week 2 button from polling to GPIO edge interrupt (debounce inside or outside the ISR — justify your choice)
- [ ] **T5.2** Convert UART RX to interrupt-driven with a small ring buffer; main loop consumes complete lines
- [ ] **T5.3** ISR discipline drill: keep every ISR under ~20 lines — set flags/queue data, never printf inside an ISR. Refactor until true
- [ ] **T5.4** Deliberately break it: remove `volatile` from a shared flag, compile with `-O2`, observe the failure. Restore and document what happened and why
- [ ] **T5.5** Write a half-page comparison in this file: polling vs. interrupts — CPU usage, latency, complexity, when you'd choose each
- [ ] **T5.6** Commit + PR "Week 5 — interrupt-driven"

## Acceptance criteria
- Button and UART both interrupt-driven; main loop is a clean event consumer
- The `volatile` experiment is documented with the observed misbehavior
- Write-up completed below

## Polling vs. interrupts write-up
(half page here)

## Notes / takeaways
