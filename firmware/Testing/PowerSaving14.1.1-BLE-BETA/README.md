## Final Testing: Power Saving 14.1.1 BLE
The firmware enables ESP32-based boards to use MeshCore BLE Companions at lower power 14-30mA instead of 80-120mA.
* One 3000mAh battery can last an ESP32-based BLE companions (Heltec v3, Xiao S3...) for 6-7 days.
* The Power Saving is set by default. No action is required.
* IoTThinks actively pushes improvements to MeshCore mainline: [MeshCore PRs by IoTThinks](https://github.com/meshcore-dev/MeshCore/issues?q=is%3Apr%20(is%3Amerged%20OR%20is%3Aopen)%20author%3A%40IoTThinks)

<img height="384" alt="image" src="https://github.com/user-attachments/assets/a08aa414-1559-4140-8099-a777d28c4d07" />
<img height="384" alt="image" src="https://github.com/user-attachments/assets/be23f499-8337-4265-8d92-b8a8be175ad8" />

Please upgrade your **easy to access devices** first.
* Download: Download **upgrade.bin** to upgrade existing devices or **freshInstall-merged.bin** for new devices.
* Instruction to [Flash Custom Firmware](https://github.com/IoTThinks/EasySkyMesh/blob/main/firmware/Instruction-to-flash-firmware.md)

Tested devices:
* Heltec v3: 21mA
* Heltec v4.2 and v4.3 (FEM ON): 25mA
* Heltec v4.3 (FEM Off): 18mA
* Xiao S3: 17A
* Xiao C3: 15mA

Please feedback your test results or ask to build for your boards
* Discord: https://discord.gg/qBZ2a8Ke
* Github: https://github.com/IoTThinks/EasySkyMesh/discussions/categories/ideas

## Love the build?
* You may buy us a cofee ☕ for good work via Paypal [![Buy me a coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-iotthinks-0070ba?style=flat&logo=paypal&logoColor=white&labelColor=0070ba&color=555555)](https://www.paypal.com/paypalme/iotthinks/9usd) or Github [![Sponsor](https://img.shields.io/badge/Sponsor-iotthinks-ea4aaa?style=flat&logo=github-sponsors&logoColor=white&labelColor=ea4aaa&color=555555)](https://github.com/sponsors/IoTThinks).
We can buy more test boards and test sensors for development.
Enjoy MeshCore. 👯‍♂️ 
