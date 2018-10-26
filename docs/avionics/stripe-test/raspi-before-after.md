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
- A 128GB FAT32-formatted flash drive was tested on all 4 USB ports and was not visible to any user on the Pi.

### General status

Aside from the notable issues with the board, the following generic status
conditions were noted:

```bash
pi@raspberrypi:~ $ lsusb
Bus 001 Device 003: ID 0424:ec00 Standard Microsystems Corp. SMSC9512/9514 Fast Ethernet Adapter
Bus 001 Device 002: ID 0424:9514 Standard Microsystems Corp. SMC9514 Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
pi@raspberrypi:~ $ lsblk
NAME        MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
mmcblk0     179:0    0 14.8G  0 disk
├─mmcblk0p1 179:1    0 43.8M  0 part /boot
└─mmcblk0p2 179:2    0 14.7G  0 part /
pi@raspberrypi:~ $ ls /dev
autofs           fd         log           mem                 ptmx   ram3     shm     tty13  tty23  tty33  tty43  tty53  tty63      vc-mem  vcsa2
block            full       loop0         memory_bandwidth    pts    ram4     snd     tty14  tty24  tty34  tty44  tty54  tty7       vcs     vcsa3
btrfs-control    fuse       loop1         mmcblk0             ram0   ram5     stderr  tty15  tty25  tty35  tty45  tty55  tty8       vcs1    vcsa4
bus              gpiochip0  loop2         mmcblk0p1           ram1   ram6     stdin   tty16  tty26  tty36  tty46  tty56  tty9       vcs2    vcsa5
cachefiles       gpiochip1  loop3         mmcblk0p2           ram10  ram7     stdout  tty17  tty27  tty37  tty47  tty57  ttyAMA0    vcs3    vcsa6
char             gpiochip2  loop4         mqueue              ram11  ram8     tty     tty18  tty28  tty38  tty48  tty58  ttyprintk  vcs4    vcsa7
console          gpiomem    loop5         net                 ram12  ram9     tty0    tty19  tty29  tty39  tty49  tty59  uhid       vcs5    vcsm
cpu_dma_latency  hwrng      loop6         network_latency     ram13  random   tty1    tty2   tty3   tty4   tty5   tty6   uinput     vcs6    vhci
cuse             initctl    loop7         network_throughput  ram14  raw      tty10   tty20  tty30  tty40  tty50  tty60  urandom    vcs7    watchdog
disk             input      loop-control  null                ram15  rfkill   tty11   tty21  tty31  tty41  tty51  tty61  vchiq      vcsa    watchdog0
fb0              kmsg       mapper        ppp                 ram2   serial1  tty12   tty22  tty32  tty42  tty52  tty62  vcio       vcsa1   zero
```
