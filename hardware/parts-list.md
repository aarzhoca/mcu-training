# Parts & Shopping List

## Core (required)
| Item | Est. cost | Notes |
|---|---|---|
| **NuMaker-M031SD EVK** | provided ✅ | M031 Cortex-M0, on-board Nu-Link2-Me debugger, Arduino UNO headers |
| USB Micro-B cable (data-capable) | $5 | Powers board + Nu-Link debug/virtual COM port |
| Breadboard + jumper wires kit | $10 | Board's Arduino headers make wiring easy |
| LEDs, resistors, push buttons kit | $10 | Board also has on-board LEDs/buttons for Weeks 1–2 |
| 10k potentiometer | $2 | Week 6 — ADC input |
| I2C temp/humidity sensor (SHT31 or AHT20 breakout) | $5–8 | Week 7 — note: 3.3V logic, matches M031 I/O |
| USB logic analyzer (8ch, Saleae-clone) | $12–15 | Week 7 — seeing real I2C/SPI bus traffic |

## Capstone: Smart Hair Clipper (recommended)
| Item | Est. cost | Notes |
|---|---|---|
| Cheap cordless hair clipper (donor) | $15–25 | Reuse motor, blade, shell |
| MOSFET motor driver breakout | $5 | Driven by M031 PWM output; never drive the motor from an MCU pin directly |
| Current-sense resistor or INA219 breakout | $3–8 | INA219 is I2C — reuses the Week 7 driver skills |
| Li-ion cell + holder + TP4056 charger board | $10 | Battery gauge via M031 ADC divider |

## Alternates
- **Robot car:** 2WD chassis kit ($20) + TB6612 driver ($5) + IR line sensors ($5) + HC-SR04 ultrasonic ($3)
- **Servo arm / pan-tilt:** 2–3 SG90 servos ($4 ea) + pan-tilt bracket ($8)

## Board & documentation links
- M031 Series BSP: https://github.com/OpenNuvoton/M031BSP
- M031 datasheet / TRM / NuMaker-M031SD user manual: nuvoton.com → M031 series product page
