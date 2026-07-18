# Week 1 — Toolchain & First Blink

**Goal:** Own the build-flash-debug loop on the NuMaker-M031SD.
**Branch:** `week1/blink` · **Reading:** M031 TRM — System Manager & Clock Controller chapters; NuMaker-M031SD schematic (find the on-board LED and button pins)

## Tasks
- [ ] **T1.1** Clone the M031 BSP; build and flash `SampleCode/StdDriver/GPIO_OutputInput`; confirm it runs
- [ ] **T1.2** In the sample's `main()`, identify and comment (in your notes below): where the system clock is configured, where the GPIO mode is set, and which register bit actually drives the pin
- [ ] **T1.3** Create your **own** project from scratch (VS Code project wizard, not a copied sample) that blinks the on-board LED at ~1 Hz using a delay loop
- [ ] **T1.4** Debugger drill: set a breakpoint in your loop, single-step, open the peripheral register view, watch the GPIO DOUT bit flip as the LED toggles. Screenshot it and drop the image in this folder
- [ ] **T1.5** Commit to this folder, open a PR titled "Week 1 — blink"

## Acceptance criteria
- LED blinks from a self-created project (not a renamed sample)
- You can explain every line of your `main()` at the check-in
- Screenshot of register view committed

## Notes / 3 takeaways
1.
2.
3.
