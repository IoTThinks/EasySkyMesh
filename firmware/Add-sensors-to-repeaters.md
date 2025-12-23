# Add sensors to repeaters
This is the instruction to add sensors to repeaters:
- The list is based on the official MeshCore firmware and the [PowerSaving MeshCore firmware](https://github.com/IoTThinks/EasySkyMesh?tab=readme-ov-file#1-powersaving-meshcore-firmware).
- The list will be updated for new sensors.
- PowerSaving firmware has powersaving feature (9mA power consumption) and additional features.

| Board  | BME280 / BME680 | Notes |
| ------------- | ------------- | ------------- |
| Heltec v3 / v4 / WSL3 | 3.3v => 3.3v <br> GND => GND <br> **41** => SDA <br> **42** => SCL <br> 3.3v => SDO  | PowerSaving works with GPIO 41,42 |
| Heltec T114 | 3.3v => 3.3v <br> GND => GND <br> **41** => SDA <br> **42** => SCL <br> 3.3v => SDO  | [Not tested yet] PowerSaving should work with GPIO 41,42 |
| RAK4631  | 3.3v => 3.3v <br> GND => GND <br> SDA => SDA <br> SCL => SCL <br> 3.3v => SDO  | Both firmwares work <br> PowerSaving has additional features |
| Xiao NRF52  | 3.3v => 3.3v <br> GND => GND <br> D7 => SDA <br> D6 => SCL <br> 3.3v => SDO  | Both firmwares work <br> PowerSaving has additional features |

### 1. BME280
The BME280 is a compact environmental sensor by Bosch that measures temperature, humidity, and barometric pressure.
* Heltec v3 and v4 does not officially expose GPIO17 and 18. Therefore, we decided to use GPIO 41 and 42 for I2C sensor.
* The default I2C address for Adafruit BME280 is 0x77. You do not need to wire 3.3v to SDO
* For other BME280 boards, you are strongly recommended to wire 3.3v to SDO to force to use address 0x77. Else, the I2C address may jump either 0x76 and 0x77.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/aef17a8b-994c-4090-84de-97d00e6d106c" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/488d290b-212e-4331-ac1a-e92bc1a964e5" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/c2f4bbce-9958-4203-a9aa-0a34634bf1f7" />

### 2. BME680
The BME680 is a compact environmental sensor by Bosch that measures temperature, humidity, barometric pressure, and air quality (gas/VOC).
* Note: As of 20 Dec 2025, MeshCore app can not show the Gas telemetry properly.
* Heltec v3 and v4 does not officially expose GPIO17 and 18. Therefore, we decided to use GPIO 41 and 42 for I2C sensor.
* The default I2C address for Adafruit BME280 is 0x77. You do not need to wire 3.3v to SDO
* For other BME680 boards, you are strongly recommended to wire 3.3v to SDO to force to use address 0x77. Else, the I2C address may jump either 0x76 and 0x77.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/3dbdafc2-af58-4304-b5b6-221cc1817ce3" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/84393dbe-8ac5-4824-9a39-0a390db8c115" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/01494234-047b-49ee-96a0-3877ed307bd9" /> 





