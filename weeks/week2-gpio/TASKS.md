# Week 2 — GPIO Inputs, Debouncing & State Machines

**Goal:** Turn your Verilog FSM knowledge into firmware state machines.
**Branch:** `week2/button-fsm` · **Reading:** M031 TRM — GPIO chapter (input modes, pull-up/pull-down); board schematic (button wiring: active-high or active-low?)

## Tasks
- [ ] **T2.1** Write a program that reads the on-board button (polling) and lights the LED while pressed. Determine from the schematic whether pressed = 0 or 1, and set the correct pull resistor
- [ ] **T2.2** Print raw button reads in a tight loop and observe switch bounce (you'll see multiple transitions per press). Note how long the bounce lasts
- [ ] **T2.3** Implement software debouncing (e.g., require N consecutive identical samples, ~10–20 ms total)
- [ ] **T2.4** Build a 3-state FSM cycled by button presses: `OFF → SLOW_BLINK → FAST_BLINK → OFF`. Use an explicit `switch(state)` structure and an enum — just like your Verilog case statement
- [ ] **T2.5** Draw the state diagram (photo of paper sketch is fine), commit it here, open PR "Week 2 — button FSM"

## Acceptance criteria
- No missed or double-counted presses (debounce works)
- FSM implemented as an explicit state machine, not nested if-spaghetti
- State diagram committed

## Notes / 3 takeaways
1.
2.
3.
