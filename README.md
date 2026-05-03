# ESP32-C3-Sensor-Hub-Soil-Moisture-BME680-VEML7700-DS18B20
A feature-packed, portable open-source hardware sensor board built around the ESP32-C3. It integrates soil moisture monitoring, environmental sensing (BME680), light sensing (VEML7700), temperature sensing (DS18B20), complete Li-ion battery management (TP4056 + DW01A Protection), and automatic power switching.
# 🌱 ESP32-C3 Multi-Sensor & Plant Monitor Board

A compact, all-in-one development board designed for effortless IoT sensing and portable applications. It features a complete suite of sensors, robust Li-ion power management, and a convenient USB-C interface.

> ⚠️ **Note:** This is an open-source hardware project. Please refer to the BOM and Pick-And-Place files for the exact components required for assembly.

---

## ✨ Key Features

*   **Core Controller:** ESP32-C3 SuperMini (also compatible with ESP32-S3 SuperMini).
*   **Sensor Suites:**
    *   **🌱 Soil Moisture:** LM393 comparator with indicator LEDs and PH Connector.
    *   **🌫️ Environmental:** BME680 (Gas, Temp, Humidity, Pressure).
    *   **☀️ Light:** VEML7700 Ambient Light Sensor (I2C).
    *   **🌡️ Temperature:** DS18B20 One-Wire Digital Sensor.
*   **Power Management (Robust):**
    *   **TP4056:** Li-ion/Li-Po battery charging over USB-C.
    *   **DW01A + FS8205A:** Over-charge/Over-discharge protection.
    *   **Auto Power Switching:** Seamless transition between USB and Battery power via DMP1045U.
*   **Connectivity & Interface:**
    *   2x Qwiic I2C connectors for easy expansion.
    *   USB-C for data and charging.
    *   Status LEDs for Power, Bluetooth, and WiFi.
*   **User Controls:** Power Switch, Reset Button, Sleep Button.

---

## 🖼️ Gallery

<img width="2357" height="833" alt="Schematic_ESP-C3-supermini-based-Project_2026-05-03" src="https://github.com/user-attachments/assets/157e8050-b478-4cff-b54d-9983fbf02d8e" />

| PCB Top | PCB Bottom | PCB 3D |
<img width="695" height="430" alt="ESP-C3 supermini based Project_3D_Top_View" src="https://github.com/user-attachments/assets/d9e3980c-4194-4ed8-8a70-9b96a84216f3" />

| :---: | :---: | :---: |

| [![PCB Top](images/PCB_Top.png)](images/PCB_Top.png) | [![PCB Bottom](images/PCB_Bottom.png)](images/PCB_Bottom.png) | [![PCB 3D](images/PCB_3D.png)](images/PCB_3D.png) |


*(Note: Ensure you place your uploaded images into an `images/` folder)*
<img width="672" height="407" alt="ESP-C3 supermini based Project_3D_Bottom_View" src="https://github.com/user-attachments/assets/4c93b192-0602-46c8-b81b-e302ae59e545" />

---
<img width="592" height="382" alt="ESP-C3 supermini based Project_2D_View" src="https://github.com/user-attachments/assets/360d9d66-edc1-4c41-a733-a5ab8811de73" />

## 📜 Schematic & PCB

*   **Schematic:** [`Schematic_ESP-C3-supermini-based-Project_2026-05-03.pdf`](Schematic_ESP-C3-supermini-based-Project_2026-05-03.pdf)
*   **PCB Layout:** [`PCB_PCB_PCB_ESP-C3-supermini-based-Project_2025-07-15_2026-05-03.pdf`](PCB_PCB_PCB_ESP-C3-supermini-based-Project_2025-07-15_2026-05-03.pdf)

---

## 📦 Bill of Materials (BOM)

The complete BOM is available in the file [`BOM_ESP-C3-supermini-based-Project_2026-05-03.csv`](BOM_ESP-C3-supermini-based-Project_2026-05-03.csv).

| Component Type | Part | Description |
| :--- | :--- | :--- |
| **MCU** | ESP32-C3 SuperMini | Main WiFi/BLE Controller |
| **Power** | TP4056, DW01A, FS8205A | Battery Charger + Protection |
| **Sensors** | BME680, VEML7700, DS18B20 | Environmental, Light, Temp |
| **UI** | LM393, LEDs, Switches | Soil Moisture Detection, Status LEDs |

---

## 🔌 Pinout & Connections

This pinout is based on the provided schematic. Please verify with the final PCB layout.

| Function | Component | Pin (ESP32-C3 SuperMini) |
| :--- | :--- | :--- |
| **I2C** | SDA (VEML7700, BME680, Qwiic) | GPIO 5 |
| | SCL (VEML7700, BME680, Qwiic) | GPIO 4 |
| **OneWire** | DS18B20 | GPIO 2 |
| **Soil Moisture** | Digital Output (PH Connector U9) | GPIO 9 (SPI_CS1) |
| **Status LEDs** | WiFi Indicator (LED1) | GPIO 12 |
| | Bluetooth Indicator (LED2) | GPIO 13 |
| **Power** | Auto Power Switching P-MOSFET (Q1) | GPIO 0 |

*(Note: Pin mappings are based on the schematic. Refer to the ESP32-C3 datasheet for alternative configurations or if using the ESP32-S3 module).*

---

## 🛠️ Getting Started / Programming

1.  **Order the PCB:** Upload the `PCB_PCB_PCB...pdf` to a manufacturer like JLCPCB or PCBWay.
2.  **Solder Components:** Assemble the board using the BOM and Pick-And-Place CSV file.
3.  **Code Setup:**
    *   Select the `ESP32C3 Dev Module` in Arduino IDE or PlatformIO.
    *   **Libraries:**
        *   `Adafruit BME680`
        *   `Adafruit VEML7700`
        *   `OneWire` & `DallasTemperature` (for DS18B20).
4.  **Upload:** Connect via USB-C, select correct COM port, and upload your code.

---

## 📂 Repository Structure
