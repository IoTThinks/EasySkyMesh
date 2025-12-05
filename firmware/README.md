# Feature Meshcore Firmware - More features
Feature firmware files are for Meshcore. 
* Have more experimental, advances features and bug fixes.
* These features will be pushed to MeshCore to merge to the main development.

## Have Suggestion?
* To make the firmware better, you can **suggest us** your wanted features [HERE](https://github.com/IoTThinks/EasySkyMesh/discussions/categories/ideas)

## Support
* The firmware is provided as it is without any warranty or support.
* If you want to support us or want custom firmware or get your bug fixed, visit [HERE](https://github.com/sponsors/IoTThinks).

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

### Power Saving 06
Based on MeshCore v1.10.0 (main).
* New Features: Added temperature to telemetry using built-in temperature sensor on ESP32-S3 and NRF52840. This is to monitor the heat inside the boxes of Solar Repeaters under the Sun.
* Known issue: Xiao S3 can not sleep due to its DIO1 is mapping to non-RTC GPIO39.
* Source code: https://github.com/IoTThinks/MeshCore/tree/powersaving
<img height="384" alt="image" src="https://github.com/user-attachments/assets/179d177b-c2f2-409b-9732-6dfd2b71cead" />
<img height="384" alt="image" src="https://github.com/user-attachments/assets/90a58e51-f528-4d76-9be1-e5d12d7c9553" />

### Power Saving 05
Based on MeshCore v1.10.0 (main). Fixed OTA via WiFi.
* Fixed: To wake up 2 minutes during FIRST boot or restart. This is to allow Repeater Setup via UART / Serial cable.
* Known issue: The clock drifts in 3 minutes in advance due to slow clock of ESP32 during light sleep.
* Source code: https://github.com/IoTThinks/MeshCore/tree/powersaving

### Power Saving 04
Based on MeshCore v1.10.0 (main). Fixed OTA via WiFi.
* Do not sleep when WiFi is not off likely due to OTA via WiFi. 
* To reboot to out of OTA and back to powersaving mode.
* Power saving mode: Still 10mA.
* OTA mode: 100mA due to WiFi. You MUST reboot to exit OTA to back to power saving mode if not doing OTA.
* Source code: https://github.com/IoTThinks/MeshCore/tree/powersaving

### Power Saving 03
Based on MeshCore v1.10.0 (main). 9mA power consumption with no latency.
* To use light sleep instead of deepsleep
* No latency due to quicker wakeup
* First boot: To wake up for 30s to send an advert at 18th second.
* Light sleep: To wake up when receiving a LoRa packet and light sleep again after 5s.
* Periodically wakeup: To wake up every 30 minutes to do some periodically tasks and and lightsleep again after 5s.
* Known issue: OTA via WiFi is not working yet.
* Source code: https://github.com/IoTThinks/MeshCore/tree/powersaving

<img height="384" alt="image" src="https://github.com/user-attachments/assets/d968ed38-9965-487e-a02e-7a571f7e7d90" />

### Power Saving 02
Reduced more power consumption. Optimized OLED, adverts and shorter operation time.
* Based on MeshCore repeater v1.9.1 - main branch
* In normal start / reset: To wake up 30s to allow sending an advert. To power on OLED for a while.
* When waken up from deepsleep: To sleep again in 5s. No OLED. No advert.
* Known issues: Only send one advert at first boot or reset. OTA via WiFi is not working.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/203c3459-5d14-4848-98d2-f75acdcfbf3e" />

### Power Saving 01
Reduced from 47mA down to 7mA. 
* Based on MeshCore repeater v1.9.1 - main branch
* To deepsleep after 2 minutes.

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

