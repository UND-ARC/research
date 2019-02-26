**[Back to Avionics](https://und-arc.github.io/research/avionics/index.html)**

# Avionics Hardware

- [Arduino](#arduino)  
- [Raspberry Pi](#raspberry-pi)   
- [M3 Avionics](#m3-avionics)  
- [Pixhawk](#pixhawk)  
- [Beaglebone](#beaglebone)  
  - [Beaglebone Blue](#blue)
  - [Beaglebone Black](#black)
  - [Beaglebone Enhanced](#enhanced)


## Arduino

| Pros          | Cons          |
| ------------- | ------------- |
| Familiar language: C | No concurrency/multithreading |
| Small & lightweight | More work to accomplish high-level tasks |
| Bare-metal programming, good for motors | Bare-metal programming -> less readable |
| Hardware interrupts | No onboard write storage |

### Known examples

- [Arduino powered rocket guidance system](https://www.instructables.com/id/Arduino-Powered-Rocket-Guidance-System/)
- [MIT CDR mentioning Arduino](http://web.mit.edu/rocketteam/www/usli/2011-12/MIT%20RT%20CDR%202012.pdf)

## Raspberry Pi

[More data/abbreviated specsheet here](https://und-arc.github.cio/research/avionics/raspberrypi.md)

| Pros          | Cons          |
| ------------- | ------------- |
| Any language | Runs operating system: background task interference |
| Concurrency/multithreading | Vibration concerns |
| High-level programming | High-level programming -> inefficient? |
| Onboard read-write storage | No hardware interrupts |

<div style="text-align:center">
    <!-- sorry about this if you're reading this file as text or offline... -->
    <img src="https://github.com/und-arc/Research/raw/master/docs/avionics/pi-pinout-diagram.png"/>
</div>

### Known examples

- [Stripped-down Pi on small rocket](https://www.raspberrypi.org/blog/rocket-man/)
- [Another reference to the same thing](http://realflightsystems.com/wordpress/?page_id=722)

## M3 Avionics

| Pros          | Cons          |
| ------------- | ------------- |
| Open-source | Designed around somebody else's rocket |
| | Poorly documented |
| | Appears large and heavy |

## Pixhawk

| Pros          | Cons          |
| ------------- | ------------- |
| High level of sensor integration | Designed for drones, not rockets |
| Vibration design considerations | Unfamiliar programming environment |
| High level of redundancy | Expensive |
| Many variations | Many variations |

Link to main page: [Pixhawk](http://pixhawk.org/)

I could not find any examples of Pixhawk being used in spaceflight, however it is very common in the UAS industry.  UND owns several Pixhawk avionics units.

## Beaglebone

Small SOC Linux-based computers.  Comes in multiple variations.

### Blue

Designed for robotics.

| Pros          | Cons         |
| ------------- | ------------ |
| High level of sensor integration | Not designed for high vibration |
| Extensive documentation | Expensive (not very) |
| Runs Debian Linux |

**Link to page:** [BeagleBone Blue](https://beagleboard.org/blue)

### Black

Designed for general-purpose computations.

| Pros           | Cons        |
| -------------- | ----------- |
| Large number of I/O pins | Not designed for high vibration |
| Small size | Not designed for sensor integration |
| Integrated WiFi |

<div style="text-align:center">
    <!-- sorry about this if you're reading this file as text or offline... -->
    <img src="https://github.com/und-arc/Research/raw/master/docs/avionics/beaglebone-black-pinout.jpg"/>
</div>

**Link to page:** [BeagleBone Black](http://beagleboard.org/black)

**[Vanderbilt CDR using BBB](https://www.vanderbilt.edu/usli/wp-content/uploads/sites/146/2016/09/CDR-1.pdf)**

### Enhanced

Designed to be an "enhanced" version of the [BeagleBone Black](#black).

| Pros          | Cons          |
| ------------- | ------------- |
| Onboard sensors | Not designed for high vibration |
| Onboard WiFi/BT | Hard to find for purchase |
| Large number of I/O pins |
| Inexpensive (~$70) |

**Link to page:** [BeagleBone Enhanced](https://www.sancloud.co.uk/?page_id=254)  
Check the dropdown menu labelled "BeagleBone Enhanced" for more hardware extensions (extra antennas, rechargeable batteries)
