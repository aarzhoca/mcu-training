# MCU Embedded Development Training

An 8-week hands-on embedded firmware training program on the **Nuvoton NuMaker-M031SD** platform (Arm Cortex-M0), mentored by Aaron Zhou.

## Who this is for
A CE/EE student with basic MCU programming, digital circuits, and Verilog/state-machine background, ramping up to practical, industry-style firmware development.

## Toolchain
- **Board:** Nuvoton **NuMaker-M031SD** EVK — M031 series Cortex-M0 @ 48 MHz, on-board Nu-Link2-Me debugger, Arduino UNO-compatible headers
- **IDE:** VS Code + Nuvoton NuMicro extensions (GCC toolchain) — see `docs/setup-guide.md` and the VS Code guide in `docs/`
- **BSP:** Official M031 Series BSP — https://github.com/OpenNuvoton/M031BSP
  - Peripheral examples live in `SampleCode/StdDriver/` (GPIO, UART, TIMER, PWM, ADC, I2C, SPI — everything this program uses)
- **Docs:** M031 datasheet & Technical Reference Manual — download from nuvoton.com (M031 series product page)
- **Debug:** On-board Nu-Link2-Me (SWD); no external probe needed

## How this repo works
- 📅 **Syllabus:** `docs/syllabus.md` — the full 8-week plan
- 🖥️ **Training materials:** `docs/slides/` — hands-on training decks; `docs/` — VS Code setup guide
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
2. Every peripheral starts with 20–30 min in the M031 Technical Reference Manual.
3. Ask questions in the Issue thread so answers are searchable later.
4. Weekly 30-min check-in: demo, one thing learned, one thing confusing.
