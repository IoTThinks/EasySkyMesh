# Add sensors to repeaters
This is the instruction to add sensors to repeaters:
- The list is based on the official MeshCore firmware and the [PowerSaving MeshCore firmware](https://github.com/IoTThinks/EasySkyMesh?tab=readme-ov-file#1-powersaving-meshcore-firmware).
- The list will be updated for new sensors.

PowerSaving firmware has powersaving feature and additional features.
- **9mA** power consumption for most ESP32S3 boards (Except Xiao S3)
- **8.5mA** power consumption for all NRF52 boards.

## 1. Quick Wiring
For PowerSaving 13 and above, you can enter CLI "sensor" to check I2C and GPS Serial pins
* PowerSaving 13+ automatically selects addresses for BME280/680/BMP280 for you.

<img height="512" alt="image" src="https://github.com/user-attachments/assets/060dd847-5984-4dc2-a5fe-cfe81180dc6c" /> 
<img height="512" alt="image" src="https://github.com/user-attachments/assets/49f25de7-a122-480f-a54a-a7176ec25f26" />


This is the wiring for some common boards:
* PowerSaving 13+ automatically selects addresses 0x76 or 0x77 for BME280/680/BMP280 for you.

| Board  | Wiring for I2C sensors | Notes |
| ------------- | ------------- | ------------- |
| Heltec v3 / v4 / WSL3 | 3.3v => 3.3v <br> GND => GND <br> 17 => SDA <br> 18 => SCL | The GPIO17 and 18 are tiny pads at bottom board. <br> Check the [notes](https://github.com/IoTThinks/EasySkyMesh/blob/main/firmware/Add-sensors-to-repeaters.md#heltec-v3) <br> <br>  Not required for PowerSaving 13+ <br> GND => SDO (BME280/680) |
| Heltec T114 | 3.3v => 3.3v <br> GND => GND <br> **P0.8** => SDA <br> **P.07** => SCL | <br>  Not required for PowerSaving 13+ <br> GND => SDO (BME280/680)|
| RAK4631  | 3.3v => 3.3v <br> GND => GND <br> SDA => SDA <br> SCL => SCL | Not required for PowerSaving 13+ <br> |
| Xiao NRF52  | 3.3v => 3.3v <br> GND => GND <br> D7 => SDA <br> D6 => SCL | Not required for PowerSaving 13+ <br> |
| Xiao S3  | 3.3v => 3.3v <br> GND => GND <br> D4 => SDA <br> D5 => SCL | Not required for PowerSaving 13+ <br> |

## 2. Boards
This section is for boards with some notes.

### Heltec v3
On Heltec v3, the GPIO17 and 18 are tiny pads in the middle of the board bottom.
- It is small. So solder with care.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/deb1808f-db8e-4134-bf51-b42ed2a308bc" />

## 3. I2C Sensors
This is the list of sensors currently supported by official MeshCore firmware.
- You may need to do some solder to make sure the sensors use the pre-defined I2C addresses.

### 3.1 GPS
This is for GPS sensor.
- For RAK boards: PIN_GPS_TX => 15 and PIN_GPS_RX => 16
- For other boards: Enter CLI "sensor" to see the TX and RX GPIOs.

### 3.2 AHTX0
This is AHT10 and AHT20 Humidity and Temperature Sensor.
- I2C address: 0x38

### 3.3 BME680
The BME680 is a compact environmental sensor by Bosch that measures temperature, humidity, barometric pressure, and air quality (gas/VOC).
* I2C address: **0x76**

<img height="384" alt="image" src="https://github.com/user-attachments/assets/3dbdafc2-af58-4304-b5b6-221cc1817ce3" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/84393dbe-8ac5-4824-9a39-0a390db8c115" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/01494234-047b-49ee-96a0-3877ed307bd9" /> 

### 3.4 BME280
The BME280 is a compact environmental sensor by Bosch that measures temperature, humidity, and barometric pressure.
* I2C address: **0x76**

<img height="384" alt="image" src="https://github.com/user-attachments/assets/aef17a8b-994c-4090-84de-97d00e6d106c" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/488d290b-212e-4331-ac1a-e92bc1a964e5" /> <img height="192" alt="image" src="https://github.com/user-attachments/assets/d25c808f-5e58-4a0f-89ea-56e70fef6efb" />

### 3.5 BMP280
BMP280 is a Bosch barometric pressure + temperature sensor (no humidity).
* I2C address: **0x76**

### 3.6 SHTC3
SHTC3 is a Sensirion temperature + humidity sensor, optimized for ultra-low power designs.
* I2C address: **0x70**

### 3.7 SHT4X
SHT4x (SHT40 / SHT41 / SHT45) is Sensirion’s newer temperature + humidity sensor family, replacing SHTC3/SHT3x for many designs.
* I2C address: **0x44**

### 3.8 LPS22HB
LPS22HB is an STMicroelectronics barometric pressure + temperature sensor, commonly used in low-power IoT designs.
* I2C address: **0x5C**

### 3.9 INA3221
INA3221 is a Texas Instruments 3-channel shunt voltage & bus voltage monitor, often used for power and battery monitoring.
* I2C address: **0x42**

### 3.10 INA219
INA219 is a Texas Instruments single-channel current, voltage, and power monitor—simple, popular, and well-supported.
* I2C address: **0x40**

### 3.11 INA260
INA260 is a Texas Instruments current, voltage, and power monitor with an integrated precision shunt resistor, making it much easier to use than INA219/INA226.
* I2C address: **0x41**

### 3.12 INA226
INA226 is a Texas Instruments high-precision current, voltage, and power monitor, more accurate and flexible than INA219, and widely used in power profiling.
* I2C address: **0x44**

### 3.13 MLX90614
MLX90614 is a Melexis non-contact infrared (IR) temperature sensor, widely used for surface and body temperature measurement.
* I2C address: **0x5A**

### 3.14 VL53L0X
VL53L0X is an STMicroelectronics Time-of-Flight (ToF) laser distance sensor, very popular for short-range, accurate distance measurement.
* I2C address: **0x29**

### 3.15 BMP085
BMP085 is an older Bosch barometric pressure + temperature sensor (the predecessor to BMP180 / BMP280).
* I2C address: **0x77**



