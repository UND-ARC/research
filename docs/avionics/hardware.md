**[Back to Avionics](https://und-arc.github.io/research/avionics/index.html)**

# Avionics Hardware

[Arduino](#arduino)  
[Raspberry Pi](#raspberry-pi)   
[M3 Avionics](#m3-avionics)  
[Pixhawk](#pixhawk)  

## Arduino

| Pros          | Cons          |
| ------------- | ------------- |
| Familiar language: C | No concurrency/multithreading |
| Small & lightweight | More work to accomplish high-level tasks |
| Bare-metal programming, good for motors | Bare-metal programming -> less readable |
| Hardware interrupts | No onboard write storage |

### Known examples

- https://www.instructables.com/id/Arduino-Powered-Rocket-Guidance-System/
- http://web.mit.edu/rocketteam/www/usli/2011-12/MIT%20RT%20CDR%202012.pdf

## Raspberry Pi

| Pros          | Cons          |
| ------------- | ------------- |
| Any language | Runs operating system: background task interference |
| Concurrency/multithreading | Vibration concerns |
| High-level programming | High-level programming -> inefficient? |
| Onboard read-write storage | No hardware interrupts |


### Known examples

- https://www.raspberrypi.org/blog/rocket-man/ / http://realflightsystems.com/wordpress/?page_id=722

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

Link to main page: http://pixhawk.org/

I could not find any examples of Pixhawk being used in spaceflight, however it is very common in the UAS industry.  UND owns several Pixhawk avionics units.
