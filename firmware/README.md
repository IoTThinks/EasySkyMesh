# Feature Meshcore Firmware - More features
Feature firmware files are for Meshcore. 
* Have more experimental, advances features and bug fixes.
* These features will be pushed to MeshCore to merge to the main development.

## Have Suggestion?
* To make the firmware better, you can **suggest us** your wanted features [HERE](https://github.com/IoTThinks/EasySkyMesh/discussions/categories/ideas)

## Pre-compiled binary files: 
* Download at [RELEASES](https://github.com/IoTThinks/MeshCore/releases/)
* Please check the [**Instruction to flash custom firmware**](https://github.com/IoTThinks/EasySkyMesh/blob/main/firmware/README.md#instruction-to-flash-custom-firmware) below.

## Repeaters
The latest firmware is on **TOP**.
* You can check the Version in MeshCore App > Remote management to confirm the flashed verion.

### Power Saving 07 - 05 Dec 2025
Improved power saving and added built-in temperature for ESP32S3 and NRF52 repeaters
- Based on MeshCore repeater v1.11.0
- ESP32S3 boards: Heltec v3 and Heltec v4
- NRF52 boards: RAK4631, Heltec T114 and T-Echo/T-Echo Lite
- Powersaving: **9mA** for ESP32 boards and **8.5mA** for NRF52 boards. You need to measure at the battery cable (NOT from USB cable).
- Built-in temperature in telemetry for ESP32S3 and NRF52 repeaters.

Bin files, release notes and source code here: https://github.com/IoTThinks/MeshCore/releases/tag/PowerSaving07

## Instruction to flash custom firmware
### For ESP32-S3 based boards (Heltec v3, Heltec v4...)
* To download **.bin** if you already flashed a repeater firmware before and want to KEEP the settings. Do NOT erase device if you want to keep the existing configuration
* To download  **-merged.bin** if you flash for the FIRST TIME or you want to ERASE the flash and settings.
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
<img height="384" alt="image" src="https://github.com/user-attachments/assets/d75c1b40-a349-488f-b623-77fbab06ddca" />
* Click Flash
<img height="384" alt="image" src="https://github.com/user-attachments/assets/a783b5a6-494e-44f7-b38c-63e4277039e1" />

### For NRF52840 based boards (RAK4631, T-Echo, T-Echo Lite...)
* To download **.zip** file
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
* Click Enter DFU mode
* Do NOT erase device if you want to keep the existing configuration
* Select the downloaded bin file
* Click Flash.
<img height="384" alt="image" src="https://github.com/user-attachments/assets/de4eb8ac-e90d-44c2-91a3-2977cfecdf85" />

## Support
* The firmware is provided as it is without any warranty or support.
* If you want to support us or want custom firmware or get your bug fixed, visit [HERE](https://github.com/sponsors/IoTThinks).
