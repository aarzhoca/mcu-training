# Week 7 — I2C / SPI & Datasheet-Driven Drivers

**Goal:** Write a real device driver from a datasheet, and see the bus with your own eyes.
**Branch:** `week7/i2c-driver` · **Hardware:** I2C temp/humidity breakout (SHT31 or AHT20) + logic analyzer. **Reading:** M031 TRM — I2C chapter; the *sensor's* datasheet (command set, timing); BSP sample `I2C_Master`

## Tasks
- [ ] **T7.1** Wire the sensor (SDA/SCL + pull-ups — check if the breakout has them onboard) and run an I2C address scan (loop addresses 0x08–0x77, print ACKs). Confirm the address matches the datasheet
- [ ] **T7.2** Hook the logic analyzer to SDA/SCL; capture the scan and identify on the waveform: START, address+R/W bit, ACK/NACK, STOP. Save a capture screenshot here
- [ ] **T7.3** From the sensor datasheet, implement `sensor_init()`, `sensor_read_temp()`, `sensor_read_humidity()` as a clean two-file driver (`sensor.c/.h`) — no BSP sample copy-paste; the sample is reference only
- [ ] **T7.4** Handle at least two failure modes gracefully: sensor unplugged (NACK) and checksum/CRC error if the part provides one
- [ ] **T7.5** Integrate: print temperature every 2 s via your event loop; `STATUS` command now includes temperature
- [ ] **T7.6** Commit + PR "Week 7 — I2C sensor driver" with the analyzer screenshot

## Acceptance criteria
- Driver is your own code, structured as a reusable module with a clean header API
- Unplugging the sensor produces an error message, not a hang
- You can point to START/ACK/STOP on your captured waveform

## Notes / takeaways
