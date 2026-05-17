 ESP32 USB-C Development Board

A compact, custom-designed ESP32 development board featuring a USB-C port for power delivery and programming. Built for makers, hobbyists, and engineers working on IoT, wireless, and embedded applications.
Features

- Microcontroller:** ESP32 (dual-core Xtensa LX6, up to 240 MHz)
- Connectivity:** Wi-Fi 802.11 b/g/n + Bluetooth 4.2 / BLE
- USB Interface:** USB-C port for power and serial programming
- Flash Memory:** 4MB (expandable depending on variant)
- GPIO: Multiple digital I/O, ADC, DAC, SPI, I2C, UART, PWM
- Power Supply:5V via USB-C or external 3.3V regulated input
- Onboard LED:Status indicator
- Reset & Boot Buttons:For easy flashing and debugging
- Compact Form Factor:Breadboard-friendly pinout

Board Pinout
Requirements

- [Arduino IDE](https://www.arduino.cc/en/software) or [PlatformIO](https://platformio.org/)
- ESP32 board support package
- USB-C cable (data-capable)
- CP2102 / CH340 driver (if needed by your OS)

Installing ESP32 Board Support (Arduino IDE)

1. Open Arduino IDE → **File > Preferences**
2. Add this URL to "Additional Board Manager URLs":
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
3. Go to **Tools > Board > Board Manager**, search `esp32`, and install.

1. Connect the board via USB-C.
2. Select the correct **COM port** under **Tools > Port**.
3. Choose board: **ESP32 Dev Module**.
4. Upload your sketch — hold the **BOOT** button if needed during upload.

Schematic & PCB Files

> The design files are available in the `/hardware` folder.

| File | Description |
|------|-------------|
| `schematic.pdf` | Full circuit schematic |
| `pcb.kicad_pcb` | KiCad PCB layout |
| `gerbers/` | Gerber files for fabrication |
| `bom.csv` | Bill of Materials |
 Specifications

| Parameter | Value |
|-----------|-------|
| MCU | ESP32-WROOM-32 |
| CPU Speed | Up to 240 MHz |
| Flash | 4 MB |
| SRAM | 520 KB |
| Operating Voltage | 3.3V |
| Input Voltage | 5V (USB-C) |
| USB Chip | CP2102 / CH340 |
| Dimensions | ~55mm x 28mm (approx.) |
 Power

The board is powered via the **USB-C port (5V)**. An onboard **AMS1117-3.3V LDO regulator** steps down to 3.3V for the ESP32. Ensure your USB-C cable supports data transfer for programming.

## Programming Modes

| Mode | How to Enter |
|------|-------------|
| Normal Boot | Press **RESET** |
| Flash Mode | Hold **BOOT**, press **RESET**, release **BOOT** |

 Known Issues / Notes

- Some USB-C cables are charge-only — use a data-capable cable for programming.
- The onboard LDO may get warm under heavy load; keep current draw under 500mA.
- If the board isn't detected, install the appropriate USB-to-Serial driver for your OS.
 License

This project is open-source under the [MIT License](LICENSE).

## Contributing

Pull requests are welcome! If you find a bug or want to improve the design, feel free to open an issue or submit a PR.

