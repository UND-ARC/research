[Back to Avionics](https://und-arc.github.io/research/avionics.index.html)

# Raspberry Pi Flight Test

The first launch of the solid-fuel Stripe rocket will carry on-board a
Raspberry Pi 3 model B v1.2 to investigate the effects of rocket flight on
a Raspberry Pi.

## Problems before test

This particular Pi was tested before flight and found to have the following
pre-existing conditions:

- A USB socket over-current charge, noted by:
```bash
# dmesg | tail
[  983.293199] usb 1-1-port2: over-current change
[  983.549255] usb 1-1-port2: over-current change
[  983.805212] usb 1-1-port2: over-current change
[  984.061207] usb 1-1-port2: over-current change
[  984.317207] usb 1-1-port2: over-current change
[  984.573222] usb 1-1-port2: over-current change
```
- A rapidly-flashing red power indicator light, as opposed to the steady indication given by normal operations.  The light flashes approximately 5 times per second.
- A minor clicking sound mirroring the frequency of the flashing power indicator light.
- When issued a soft shutdown, the Pi's status lights indicate power ON and disk read OFF.  No flashing/clicking.
