# Instruction to flash firmware
## 1. For ESP32-S3 based boards 
Heltec v2, v3, v4, WSL3, Xiao S3, Station G2, Lilygo T3 S3...:
* To download **.bin** if you already flashed a repeater firmware before and want to KEEP the settings. Do NOT erase device if you want to keep the existing configuration
* To download **merged.bin** if you want flash a new fresh board
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
* Click Flash
<img height="384" alt="image" src="https://github.com/user-attachments/assets/a783b5a6-494e-44f7-b38c-63e4277039e1" />

## 2. For NRF52840 based boards
RAK4631, Heltec T114, T-Echo, T-Echo Lite...

### Method 1:
* To download **.zip** file
* Go to Web Flasher: https://flasher.meshcore.co.uk/
* Select Custom Firmware
* Click Enter DFU mode
* Do NOT erase device if you want to keep the existing configuration
* Select the downloaded zip file
* Click Flash.
<img height="384" alt="image" src="https://github.com/user-attachments/assets/de4eb8ac-e90d-44c2-91a3-2977cfecdf85" />


### Method 2:
* To download uf2 file.
* To press some keys to enter DFU mode and open the NRF2BOOT folder. RAK: Press RESET twice. T-echo Lite: Press RESET, wait for 1s, then press RESET.
* To drop the uf2 file in the NRF2BOOT folder
* The device will auto reboot and close the NRF2BOOT folder.
<img height="192" alt="image" src="https://github.com/user-attachments/assets/4648416a-b906-46e6-84c1-a13f3a7a2a62" />

Enjoy.
