# MCU Embedded Development Training

An 8-week hands-on embedded firmware training program on the **Nuvoton NuMaker** platform (Arm Cortex-M), mentored by Aaron Zhou.

## Who this is for
A CE/EE student with basic MCU programming, digital circuits, and Verilog/state-machine background, ramping up to practical, industry-style firmware development.

## Toolchain
- **Board:** Nuvoton NuMaker EVK (see `hardware/parts-list.md`)
- **IDE:** VS Code + Nuvoton NuMicro extensions (GCC toolchain)
- **BSP:** Official Nuvoton BSPs from https://github.com/OpenNuvoton
- **Debug:** On-board Nu-Link (SWD)

## How this repo works
- 📅 **Syllabus:** `docs/syllabus.md` — the full 8-week plan
- 📁 **Weekly work:** each `weeks/weekN-*` folder holds that week's exercise code and a `TASKS.md`
- ✅ **Assignments:** tracked as GitHub **Issues** (one per task), organized on the **Project board**
- 🔀 **Workflow:** create a branch per task → commit code → open a Pull Request → mentor reviews → merge
- 🎓 **Capstone:** `capstone/` — final integrated project (recommended: smart hair clipper controller)

## Weekly cadence
| Week | Topic | Deliverable |
|---|---|---|
| 1 | Toolchain & first blink | Self-built LED blink project, debugger walkthrough |
| 2 | GPIO & buttons | Button-driven LED state machine |
| 3 | UART & printf | UART echo + text command parser |
| 4 | Timers & PWM | LED breathing + 1 ms tick scheduler |
| 5 | Interrupts | Interrupt-driven button + UART RX |
| 6 | ADC & sensors | Sensor stream over UART, PWM tracks pot |
| 7 | I2C / SPI | Working driver for an I2C/SPI device |
| 8 | Capstone | Integrated project demo + README |

## Ground rules
1. Commit early, commit often — small commits with clear messages.
2. Every peripheral starts with 20–30 min in the Technical Reference Manual.
3. Ask questions in the Issue thread so answers are searchable later.
4. Weekly 30-min check-in: demo, one thing learned, one thing confusing.
