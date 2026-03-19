### This is for BETA features:
* Please set your expectation and be cautious.
* Always test to your test / dev devices first.
* Instruction to [Flash custom firmware](https://github.com/IoTThinks/EasySkyMesh/blob/main/firmware/Instruction-to-flash-firmware.md)

### Testing features:
#### 1. PowerSaving for ESP32-based BLE companions - 3-4 days on 3000mAh battery
* Based on PowerSaving 14 (MeshCore v1.14 + PowerSaving)
* Reduced power consumption for ESP32-based BLE companion from 12x mA down to 32-35 mA for Heltec v3 and 39mA Heltec v4.2. 
* Other ESP32-based boards should be similar but untested. Please help to test.
* BLE connection will be maintained all the times. 
* You should feel no difference and no delay compared to the stock MeshCore v1.14.

Notes:
* Heltec v4: Need to monitor stability on battery and iPhone. May stuck at 50mA on my power supply. Seem fine on USB power and battery.
* Heltec v3: Stable on battery / usb cable with Android phone.

<img height="384" alt="image" src="https://github.com/user-attachments/assets/b6d96d71-fb78-46bd-a134-51c34a8a79be" />
<img height="384" alt="image" src="https://github.com/user-attachments/assets/326e16cd-42f5-448e-9211-4dc197b9b404" />
<img height="384" alt="image" src="https://github.com/user-attachments/assets/95364ae0-40f4-4fb5-8a46-688101de37cf" />


