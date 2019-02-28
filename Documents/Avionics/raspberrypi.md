# Raspberry Pi Specifications

## RPi 3B

This section details the Raspberry Pi 3B.

| Metric | Notes | Min | Typical | Max | Units |
| ------ | ----- | --- | ------- | --- | ----- |
| Length |       |     |   85.6  |     |  mm   |
| Width  |       |     | 56      |     |  mm   |
| Height |       |     | 21      |     |  mm   |
| Weight |       |     | 42      |     |  gram |
| Power draw |   | 260 | 480     | 730 |  mA   |
| Disconnected power draw | Power draw while plugged in, but off | 20  |   | 30  | mA  |
| Voltage required |  | 4.75 | 5.0 | 5.25 | volt  |
| Operating temperature | Certified | 0 |   | 50 | deg. Celsius |
| Operating temperature | Tested | -107  |   | 112 | deg. Celsius |

CPU/chipset details:
 * CPU is as BCM2837 chip, 4 core, 1.2GHz, ARMv8, 64-bit
 * 1GB RAM LPDDR2
 * Networking:
   - 10/100M Ethernet
   - 2.4GHz 802.11 b/g/n WiFi, supports WEP/WPA/WPA2, AES-CCMP (max 256 bit)
   - 2.5GHz 802.15 Bluetooth 4.1, AES-128
 * GPU is a VideoCore IV chip:
   - 32-bit
   - H.264, MPEG-4 decode (1080p30), H.264 encode (1080p30), OpenGL eS1.1, 2.0
   - VideoCore normal clock speed 250 MHz, overclockable to 400MHz
   - Specs are guaranteed, likely to do better in real world

## RPi 3B+

This section details the Raspberry Pi 3B+.

| Metric | Notes | Min | Typical | Max | Units |
| ------ | ----- | --- | ------- | --- | ----- |
| Length |       |     |   85.6  |     |  mm   |
| Width  |       |     | 56      |     |  mm   |
| Height |       |     | 21      |     |  mm   |
| Weight |       |     | 42      |     |  gram |
| Power draw |   | 350 | 950     | 980 |  mA   |
| Disconnected power draw | Power draw while plugged in, but off | 20  |   | 30  | mA  |
| Voltage required |  | 4.75 | 5.0 | 5.25 | volt  |
| Operating temperature | Certified | 0 |   | 50 | deg. Celsius |
| Operating temperature | Tested | -107  |   | 112 | deg. Celsius |

CPU/chipset details:
 * CPU is a BCM2837B0 chip, 4 core, 1.4GHz, ARMv8
 * 1GB RAM LPDDR2
 * Networking:
   - 100/1000M Ethernet (over USB2.0 - max throughput 300Mbit/sec)
   - 2.4GHz & 5GHz 802.11 b/g/n/ac WiFi, supports WEP/WPA/WPA2, AES-CCMP (max 256 bit)
   - 2.5GHz 802.15 Bluetooth 4.2, BLE
 * GPU is a VideoCore IV chip
   - 32-bit
   - H.264, MPEG-4 decode (1080p30), H.264 encode (1080p30), OpenGL eS1.1, 2.0
   - VideoCore normal clock speed 250 MHz, overclockable to 400MHz
   - Specs are guaranteed, likely to do better in real world
