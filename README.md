<img width="1920" height="2560" alt="photo_2026-10-18_11-41-16" src="https://github.com/user-attachments/assets/339e7977-8295-4424-a43f-3cc5859c899e" />

# Smart Kettle — ESPHome

ESPHome firmware for the Xiaomi Kettle Pro 3 smart kettle based on ESP32-S2. Displays temperature and water level using load cells.

## Features

- Heating control (relay + SCR) via Home Assistant and touch buttons
- NTC temperature measurement (GPIO9)
- HX711 weight measurement (water level)
- ST7735 128×115 display with water level, temperature, time, and heating icon
- Touch buttons: heating on/off, mode switching (40→60→80→99 °C)
- Buzzer: button press confirmation, error signals, heating completion signal
- Fallback access point (captive portal) when Wi-Fi is lost
- Static IP

## Hardware

| Component | Pins |
|-----------|------|
| Heating relay | GPIO1 |
| SCR triac | GPIO5 |
| Heating LED | GPIO17 |
| Mode LEDs | GPIO12 |
| Display backlight | GPIO2 |
| Display (SPI) | CLK GPIO36, MOSI GPIO35, CS GPIO34, DC GPIO21, RST GPIO40 |
| HX711 | DOUT GPIO16, CLK GPIO18 |
| NTC | GPIO9 (ADC) |
| Buzzer | GPIO7 (LEDC) |
| Touch "heating" | GPIO4 |
| Touch "modes" | GPIO11 |
| Zero-cross | GPIO3 |
