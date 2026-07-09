# Environment Setup Guide

## 1. Install tools
1. **VS Code** — https://code.visualstudio.com
2. **Nuvoton NuMicro VS Code extension** — search "Nuvoton" in the VS Code marketplace; it installs the GCC toolchain, OpenOCD/Nu-Link support, and project wizard
3. **Git** — https://git-scm.com
4. **Serial terminal** — VS Code Serial Monitor extension or PuTTY

## 2. Get the BSP
Clone the BSP for your board from https://github.com/OpenNuvoton (e.g., the M251/M460 series BSP). Browse `SampleCode/StdDriver/` — this is your example library for the whole program.

## 3. First flash
1. Connect the NuMaker board via USB (Nu-Link debugger port)
2. Open a BSP GPIO sample in VS Code, build, flash
3. Confirm the LED blinks — you're in business

## 4. Repo workflow
```bash
git clone <this repo>
git checkout -b week1/blink
# ...work...
git add . && git commit -m "week1: LED blink working"
git push -u origin week1/blink
# open a Pull Request on GitHub for review
```

## Troubleshooting
- Board not detected → check Nu-Link driver / try another USB cable (must be data-capable)
- Build errors after cloning BSP → verify the extension installed the Arm GCC toolchain (check VS Code output panel)
