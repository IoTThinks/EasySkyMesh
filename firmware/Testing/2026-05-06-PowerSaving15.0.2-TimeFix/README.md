To drift forward less than 7s/day (3.5 minutes/month) for ESP32-based repeaters with Power Saving:
* Wake up every 30s to stabilize slow clock
* CLI "clock" now returns time with seconds. This is to validate with https://time.is/
