# Add sensors to repeaters
This is the instruction to add sensors to repeaters:
- The list is based on the official MeshCore firmware and the [PowerSaving MeshCore firmware](https://github.com/IoTThinks/EasySkyMesh?tab=readme-ov-file#1-powersaving-meshcore-firmware).
- The list will be updated for new sensors.
- PowerSaving firmware has powersaving feature (9mA power consumption) and additional features.

## 1. Quick Wiring
| Board  | Wiring for I2C sensors | Notes |
| ------------- | ------------- | ------------- |
| Heltec v3 / v4 / WSL3 | 3.3v => 3.3v <br> GND => GND <br> 17 => SDA <br> 18 => SCL <br><br> GND => SDO (BME280/680)  | On Heltec v3, the GPIO17 and 18 are tiny pads in the middle of the board bottom. |
| Heltec T114 | 3.3v => 3.3v <br> GND => GND <br> **0.16** => SDA <br> **0.13** => SCL <br><br> GND => SDO (BME280/680)| Not tested yet |
| RAK4631  | 3.3v => 3.3v <br> GND => GND <br> SDA => SDA <br> SCL => SCL <br><br> GND => SDO (BME280/680) | Both firmwares work <br> PowerSaving has additional features |
| Xiao NRF52  | 3.3v => 3.3v <br> GND => GND <br> D7 => SDA <br> D6 => SCL <br><br> GND => SDO (BME280/680) | Both firmwares work <br> PowerSaving has additional features |
| Xiao S3  | 3.3v => 3.3v <br> GND => GND <br> D4 => SDA <br> D5 => SCL <br><br> GND => SDO (BME280/680) | Both firmwares work <br> PowerSaving has additional features |

## 2. Boards
This section is for boards with some notes.

### Heltec v3
On Heltec v3, the GPIO17 and 18 are tiny pads in the middle of the board bottom.
- It is small. So solder with care.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/deb1808f-db8e-4134-bf51-b42ed2a308bc" />

## 3. I2C Sensors
This section will be updated to include all supported sensors.

### BME280
The BME280 is a compact environmental sensor by Bosch that measures temperature, humidity, and barometric pressure.
* MeshCore requires I2C address **0x76** for BME280
* For Adafruit BME280, you need to solder the Addr pad to use I2C address 0x76
* For other BME280 boards, you are strongly recommended to wire **GND to SDO** to force to use address 0x77. Else, the I2C address may jump either 0x76 and 0x77.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/aef17a8b-994c-4090-84de-97d00e6d106c" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/488d290b-212e-4331-ac1a-e92bc1a964e5" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/d25c808f-5e58-4a0f-89ea-56e70fef6efb" />

### BME680
The BME680 is a compact environmental sensor by Bosch that measures temperature, humidity, barometric pressure, and air quality (gas/VOC).
* Note: As of 20 Dec 2025, MeshCore app can not show the Gas telemetry properly in Channel 1 or 2.
* MeshCore requires I2C address **0x76** for BME680
* For Adafruit BME280, you need to solder the Addr pad to use I2C address 0x76.
* For other BME280 boards, you are strongly recommended to wire **GND to SDO** to force to use address 0x77. Else, the I2C address may jump either 0x76 and 0x77.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/3dbdafc2-af58-4304-b5b6-221cc1817ce3" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/84393dbe-8ac5-4824-9a39-0a390db8c115" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/01494234-047b-49ee-96a0-3877ed307bd9" /> 

