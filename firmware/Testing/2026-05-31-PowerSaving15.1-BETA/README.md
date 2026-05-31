## This is PowerSaving 15.1 BETA:
- Based on MeshCore 1.15 and PowerSaving 15.0.x

### Change logs:
- For NRF52, added feature to keep time across resets. This is to keep receiving adverts even after a reset / fault or after periodical reboots. This is already implemented in ESP32 for PowerSaving variant.
- For repeaters, added CLI to automatically reboot: **set reboot.interval <hours>** and **get reboot.interval**. <hours> is 0-255. 0 is disabled.

### Demo:
- RAK4631 repeater reboots after 1 hour and still keep the time.
<img height="512" alt="image" src="https://github.com/user-attachments/assets/637cb2b1-edc1-47db-91b9-b4a0e0cffa00" />
<img height="512" alt="image" src="https://github.com/user-attachments/assets/4e6f1e79-cb60-400f-9d6a-e18b230decdf" />


