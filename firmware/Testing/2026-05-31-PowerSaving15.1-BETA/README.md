## This is PowerSaving 15.1 BETA:
- Based on MeshCore 1.15 and PowerSaving 15.0.x

Change logs:
- For NRF52, added feature to keep time across resets. This is to keep receiving adverts even after a reset / fault or after automatically reboots. This is already implemented in ESP32 for PowerSaving variant.
- For repeaters, added CLI to automatically reboot: **set reboot.interval <hours>** and **get reboot.interval**. <hours> is 0-255. 0 is disabled.
