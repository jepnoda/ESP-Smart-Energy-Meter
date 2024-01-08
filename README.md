# ⚡ESP Smart Energy Meter

|     |     |
| --- | --- |
| ![device-opened](https://raw.githubusercontent.com/jepnoda/ESP-Smart-Energy-Meter/main/device-enclosed.jpg) | ![device-opened](https://raw.githubusercontent.com/jepnoda/ESP-Smart-Energy-Meter/main/device-opened.jpg) | 

A Smart Power Monitoring device, is intricately crafted, focusing on accuracy and versatility in tracking electrical parameters, such as voltage, current, power, and energy consumption.

## Core Features

This device is intended to function with **alternating current (AC)** and to monitor various electrical parameters.

- Current
- Voltage
- Frequency
- Power Factor
- Realtime Power Consumption (Watt)
- Store Power Consumption (Watt-hour)

## Prerequisites

This device was built with [ESPHome](https://esphome.io/) and is intended to work with [Home Assistant.](https://www.home-assistant.io/)

### Modules

- [ESP32 DevKit V1 MCU](https://shopee.ph/ESP-32S-ESP-WROOM-32-ESP32-ESP-32-Bluetooth-and-WIFI-Dual-Core-CPU-with-Low-Power-Consumption-MCU-ESP-32-i.580325202.14223060123?sp_atk=0641a5ae-d303-4cc2-b6fd-913253973a58&xptdk=0641a5ae-d303-4cc2-b6fd-913253973a58)
- [PZEM-004T V3](https://shopee.ph/PZEM-004T-Ac-Multi-function-Electric-Energy-Metering-Power-Monitor-Watt-Meter-i.18252381.18907013159?sp_atk=18abbf32-1601-4535-b088-0e308aa1a2b1&xptdk=18abbf32-1601-4535-b088-0e308aa1a2b1)
- [SSD1306 OLED Display Module](https://shopee.ph/0.96-inch-128x64-pixels-SSD1306-OLED-Display-Module-i.237034143.6548465016?sp_atk=789abb04-2939-47aa-a893-fea9c23f6f77&xptdk=789abb04-2939-47aa-a893-fea9c23f6f77)
- [HiLink HLK-5M05 AC/DC Buck Converter 100-240 VAC to 5 DC 1A(5W)](https://shopee.ph/HLK-5M05-HLK-5M03-HLK-5M12-5W-AC-DC-220V-to-12V-5V-3.3V-Buck-Step-Down-Power-Supply-Module-Converter-Intelligent-i.580325202.20209582747)

## Getting Started

### Pictorial Diagram

![pictorial-diagram](https://raw.githubusercontent.com/jepnoda/ESP-Smart-Energy-Meter/main/pictorial-diagram.png)

### Pin Connections

| PZEM-004T V3 Pin | SSD1306 OLED Pin | HiLink AC-DC Pin | ESP32 Devkit V1 Pin |
| :----------: | :--: | :----------: | :-------------: |
| RX | ❌ | ❌ | TX2 |
| TX | ❌ | ❌ | RX2 |
| ❌ | SCL | ❌ | D22 |
| ❌ | SDA | ❌ | D21 |
| ❌ | VCC | ❌ | 3V3 |
| VCC | ❌ | VOUT➕ | VIN |
| GND | GND | VOUT➖ | GND |

---

1. Ensure [ESPhome](https://esphome.io/guides/getting_started_hassio) and [File Editor](https://github.com/home-assistant/addons/blob/master/configurator/DOCS.md) add-ons are installed on your [Home Assistant](https://www.home-assistant.io/getting-started/) instance.
2. Ensure that your ESPHome `secrets.yaml` file is up to date.
3. Using the File Editor add-ons, upload the `esp-energy-meter.yaml` config file along with `materialdesignicons-webfont.ttf` font file on the `config/esphome/`.
4. Using the ESPHome dashboard, modify the `esp-energy-meter.yaml` and replace the **redacted** part of the config file.
5. **Build** and **upload** the firmware to your device.
6. Now, you can [integrate](https://www.home-assistant.io/getting-started/concepts-terminology/) the device into your Home Assistant.

---

### Operational Device

![device-running](https://raw.githubusercontent.com/jepnoda/ESP-Smart-Energy-Meter/main/device-running.jpg)
