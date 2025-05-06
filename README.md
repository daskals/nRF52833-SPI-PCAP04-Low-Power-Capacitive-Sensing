# nRF52833-SPI-PCAP04-Low-Power-Capacitive-Sensing

This repository contains an example application for the nRF52833 Development Kit (PCA10100) demonstrating periodic, low-power capacitive sensing using the PCAP04 capacitive-to-digital converter via SPI. The application leverages the Real-Time Counter (RTC) to wake the MCU every second and collect capacitive measurements.

## 📦 Features

* ✅ SPI communication with PCAP04 capacitive sensor IC
* ✅ RTC-triggered periodic sensing (1 second default)
* ✅ Low-power sleep mode between measurements
* ✅ UART logging via SEGGER RTT
* ✅ Configurable sampling interval and SPI settings

## 🔧 Hardware Requirements

* [nRF52833 Development Kit (PCA10100)](https://www.nordicsemi.com/Products/Development-hardware/nRF52833-DK)
* [PCAP04 Capacitive Sensing IC](https://www.ichaus.de/PCAP04)
* Capacitive sensor electrodes
* Optional: LEDs for visual feedback

## 🛠️ Software Details

* **SDK Version:** nRF5 SDK 17.1.0
* **SoftDevice:** Not required
* **Toolchain:** SEGGER Embedded Studio or GCC

## 📂 Structure

* `main.c`: Main application that initializes RTC, SPI, and triggers periodic measurements from PCAP04

## ⚙️ Sampling Strategy

* Sampling interval: 1 second (adjustable via `SAMPLE_INTERVAL_SEC` macro)
* RTC configured at 32 Hz for ultra-low-power wake-up
* SPI command issued to PCAP04 after wake-up, result logged over RTT

## ⚖️ Power Considerations

* System enters low-power mode between RTC wake-ups
* SPI and PCAP04 powered only during active measurement

## 📉 Future Extensions

* Support for multiple PCAP04 channels
* Optional averaging or filtering of measurements
* Integration with BLE for wireless capacitive data broadcasting

## 📄 License

This project uses Nordic Semiconductor’s standard SDK license.

---

## 👨‍💼 Author

Created by \[Your Name], demonstrating low-power capacitive sensing via SPI using the nRF52833 and PCAP04.

---
