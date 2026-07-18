# Week 3 — UART & printf Debugging

**Goal:** Establish serial comms — your primary debug channel for the rest of the program.
**Branch:** `week3/uart-cli` · **Reading:** M031 TRM — UART chapter (baud rate generation, FIFO); BSP sample `UART_TxRx`

## Tasks
- [ ] **T3.1** Run the BSP UART sample over the Nu-Link virtual COM port (VCOM); connect at 115200-8-N-1 with the VS Code serial monitor or PuTTY
- [ ] **T3.2** In your own project, initialize UART0 and retarget `printf` — print a hello banner with the system clock frequency
- [ ] **T3.3** Build a polled echo: every received character is sent back
- [ ] **T3.4** Upgrade to a line-based command parser supporting: `LED ON`, `LED OFF`, `LED BLINK`, `STATUS` (prints current state + uptime estimate), and a helpful error for unknown commands
- [ ] **T3.5** Bonus: change baud to 9600 and back — confirm you understand the baud rate divisor math from the TRM
- [ ] **T3.6** Commit + PR "Week 3 — UART CLI". Include a terminal-session screenshot

## Acceptance criteria
- printf works from your own project
- Parser handles backspace-free line input robustly (garbage input doesn't hang it)
- You can explain how the baud rate is derived from the clock

## Notes / 3 takeaways
1.
2.
3.
