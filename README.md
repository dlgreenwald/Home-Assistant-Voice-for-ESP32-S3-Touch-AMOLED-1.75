# Home Assistant Voice for ESP32-S3 Touch AMOLED (1.75")

A **working ESPHome voice assistant** configuration for an **ESP32-S3 with a 1.75" round AMOLED touchscreen**, microphone, speaker, wake word support, and touch input — designed as a **local Home Assistant voice front-end**.

This repo exists because **there was no complete, working YAML for this device**.

---

## ✨ Features
- ✅ Wake word support (on-device or via Home Assistant)
- ✅ Microphone + speaker (I2S)
- ✅ 1.75" round AMOLED UI (466×466)
- ✅ Touch input (tap / long-press)
- ✅ Visual feedback for listening / thinking / replying
- ✅ Timers with on-screen progress
- ✅ Fully local (ESPHome + Home Assistant)
- ✅ Media Streaming (Music Assistant)

---

## 🧠 Hardware
Tested with:
- ESP32-S3 dev board
- 1.75" round AMOLED display (QSPI, 466×466)
- CST816 / CST9217 / FT3168 touchscreen
- ES8311 DAC + ES7210 ADC (I2S audio)

> ⚠️ **This YAML is hardware-specific.**  
> If your pins, display driver, or audio chips differ, you *must* adjust them.

---

## 🚀 Quick Start (5 minutes)
1. Install **ESPHome 2026.1.0 or newer**
2. Copy the YAML file from this repo
3. Create a `secrets.yaml`:
   ```yaml
   wifi_ssid: "YOUR_WIFI"
   wifi_password: "YOUR_PASSWORD"
   ota_password: "YOUR_OTA_PASSWORD"
   api_encryption_key: "GENERATE_A_NEW_KEY"
   ```
4. In the YAML, change:
   ```yaml
   esphome:
     name: your_device_name
     friendly_name: Your Device Name
   ```
5. Flash the device
6. Add it to Home Assistant
7. Talk to it. Yes, really.

---

SDL Development Quickstart
1. Clone this repo and cd into it
2. Run `python3 -m venv .`
3. Run `source ./bin/activate`
4. Run `esphome run sdl.yaml`

More details here: https://community.home-assistant.io/t/how-to-virtual-esphome-device-and-development-using-windows-work-in-progress/802669
---

## 🔐 Security Notes
- Wi-Fi credentials and OTA passwords are stored in `secrets.yaml`
- **Do not commit real secrets**
- Rotate your API encryption key if you forked this repo

---

## ⚠️ Known Limitations
- Large YAML (not beginner-friendly)
- Hardware-specific pinout
- Display init sequence is tuned for this panel
- Expect to tweak timings if your audio hardware differs

---

## 🤝 Contributing
PRs welcome for:
- Other AMOLED panels
- Different ESP32-S3 boards
- Cleanup / modularization
- Docs and diagrams

---

## Citations

This project would not be possible without the work done by others, and largely pulls together and reuses components from the original author of this repo, and the following pages/repos.  Special thanks to the Respeaker work as it provided the soultion to media streaming.
https://devices.esphome.io/devices/waveshare-esp32-s3-touch-amoled-1.75/
https://github.com/esphome/wake-word-voice-assistants/blob/main/esp32-s3-box-3/esp32-s3-box-3.yaml
https://github.com/formatBCE/Respeaker-Lite-ESPHome-integration/blob/main/config/common/respeaker-satellite-base.yaml

---

## 🪦 Why this repo exists
Because nobody published a **complete, working** ESPHome voice assistant YAML for this hardware — so here it is.

If this helped you, **star it** so other people can find it.# ESP32-S3-Touch-AMOLED-1.75
ESPHome configuration for ESP32-S3 with 1.75" AMOLED display and touchscreen, designed as a local voice assistant front-end for Home Assistant.
