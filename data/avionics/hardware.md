# Avionics Hardware

[Arduino](#arduino)  
[Raspberry Pi](#raspberry-pi)   
[M3 Avionics](#m3-avionics)  

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
