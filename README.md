# LoRa Mesh Applications on MeshCore
We build and share custom firmware and sensor solutions for LoRa mesh networks based on Meshcore.
- We develop optimized firmware for long-range, low-power mesh deployments.
- We integrate advanced sensor modules to deliver reliable, real-time environmental and infrastructure data.
- Using Meshcore as the backbone, we create scalable IoT solutions tailored for agriculture, smart cities, and industrial automation.

Resources:
- [Tài liệu hướng dẫn cho Việt Nam](https://github.com/IoTThinks/EasySkyMesh/wiki)

## 1. PowerSaving MeshCore firmware: 
Feature firmwares are for Meshcore. They have more experimental, advances features and bug fixes. These features will be pushed to MeshCore to merge to the main development.
* Download at [RELEASES](https://github.com/IoTThinks/EasySkyMesh/releases)
* Source code changes: [Source code](https://github.com/IoTThinks/MeshCore/tags)

### Suggestion or support your boards?
* You can suggest us your wished features or have us to build the binary files for you [HERE](https://github.com/IoTThinks/EasySkyMesh/discussions/categories/ideas)

### Instruction
#### For ESP32-S3 based boards (Heltec v3, Heltec v4...)
* To download **.bin** if you already flashed a repeater firmware before and want to KEEP the settings. Do NOT erase device if you want to keep the existing configuration
* To download  **-merged.bin** if you flash for the FIRST TIME or you want to ERASE the flash and settings.
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
* Click Flash
<img height="384" alt="image" src="https://github.com/user-attachments/assets/a783b5a6-494e-44f7-b38c-63e4277039e1" />

#### For NRF52840 based boards (RAK4631, T-Echo, T-Echo Lite...)
##### Method 1:
* To download **.zip** file
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
* Click Enter DFU mode
* Do NOT erase device if you want to keep the existing configuration
* Select the downloaded zip file
* Click Flash.
<img height="384" alt="image" src="https://github.com/user-attachments/assets/de4eb8ac-e90d-44c2-91a3-2977cfecdf85" />


##### Method 2:
* To download uf2 file.
* To press some keys to enter DFU mode and open the NRF2BOOT folder. RAK: Press RESET twice. T-echo Lite: Press RESET, wait for 1s, then press RESET.
* To drop the uf2 file in the NRF2BOOT folder
* The device will auto reboot and close the NRF2BOOT folder.
<img height="192" alt="image" src="https://github.com/user-attachments/assets/4648416a-b906-46e6-84c1-a13f3a7a2a62" />


## 2. Community Support
* The firmware is provided as it is without any warranty or support.
* If you want to support us or get your bug fixed, [Sponsor Us](https://github.com/sponsors/IoTThinks).

## 3. Professional Services
* If you want custom development for your projects, [Contact Us](https://iotthinks.com/contact-us/)


