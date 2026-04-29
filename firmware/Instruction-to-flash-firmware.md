# Instruction to flash firmware
## 1. For ESP32-S3 based boards 
Heltec v2, v3, v4, WSL3, Xiao S3, Station G2, Lilygo T3 S3...
* [More often] To download **upgrade.bin** if you already flashed a repeater firmware before and want to KEEP the settings. Do NOT erase device if you want to keep the existing configuration
* To download **freshInstall-merged.bin** if you want flash a new fresh board

### Method 1: OTA
For repeaters / room servers, you can upgrade via OTA if in range of the repeaters / room servers' WiFi:
* Enter CLI "start ota"
* Connect the WiFi of your laptop to the WiFi name "MeshCore OTA"
* Open browser to http://192.168.4.1/update
* Select **upgrade.bin** file
* Click "Flash"
* You may need to click Reset button for some boards with CDC (like Heltec v4)

### Method 2: Zip file
* Go to Web Flasher: [https://meshcore.io/flasher](https://meshcore.io/flasher)
* Select Custom Firmware
<img width="1024" alt="image" src="https://github.com/user-attachments/assets/c49a9672-a99d-4267-9427-219b5e41a860" />

* Most of the case, use upgrade.bin to upgrade. Do NOT select "Erase Device"
* Click Flash
* For some boards, you need to press RESET button to start running.
<img width="1024" alt="image" src="https://github.com/user-attachments/assets/84932b28-19eb-48ef-bcfb-cebe105454cc" />

## 2. For NRF52840 based boards
RAK4631, Heltec T114, T-Echo, T-Echo Lite...

### Method 1: OTA
For repeaters / room servers, you can upgrade via OTA if in range of the repeaters / room servers's BLE
* Enter CLI "start ota"
* Use NRF Connect to upload the **upgrade.bin** file (not uf2 file)

### Method 2: Zip file
* To download **.zip** file
* Go to Web Flasher: [https://meshcore.io/flasher](https://meshcore.io/flasher)
* Select Custom Firmware
<img width="1024" alt="image" src="https://github.com/user-attachments/assets/c49a9672-a99d-4267-9427-219b5e41a860" />

* Click Enter DFU mode
* Do NOT erase device if you want to keep the existing configuration
* Select the downloaded zip file
* Click Flash.
<img width="1024" alt="image" src="https://github.com/user-attachments/assets/65eb244f-0cf4-475e-b004-407bcd552cb2" />

### Method 3: UF2 file
* To download uf2 file.
* To enter DFU mode, RAK: Press RESET twice. T-echo Lite: Press RESET, wait for 1s, then press RESET.
* To open the NRF2BOOT folder
* To drop the uf2 file in the NRF2BOOT folder
* The device will auto reboot and close the NRF2BOOT folder.
<img height="192" alt="image" src="https://github.com/user-attachments/assets/4648416a-b906-46e6-84c1-a13f3a7a2a62" />

Enjoy.
