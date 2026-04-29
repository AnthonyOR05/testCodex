# Wiring (Raspberry Pi Pico W)

## Overview
This project connects:
- 1x Raspberry Pi Pico W (RP2040)
- 1x 4x4 membrane keypad
- 12x LEDs
- 12x 220 Ω LED resistors
- 4x 1 kΩ pull-up resistors for keypad rows

All LED cathodes are tied to GND. Each LED anode goes through a 220 Ω resistor to a dedicated GPIO.

## Components list (from `diagram.json`)
- `wokwi-pi-pico` x1 (use Pico W on hardware)
- `wokwi-membrane-keypad` x1
- `wokwi-led` x12
- `wokwi-resistor` 220 Ω x12 (`r1`..`r12`)
- `wokwi-resistor` 1 kΩ x4 (`rp1`..`rp4`)

## GPIO mapping table

### Keypad matrix
| Keypad signal | Pico GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

### LEDs
| Logical LED | Label in diagram | Pico GPIO |
|---|---|---|
| ledPins[0] | 1 | GP11 |
| ledPins[1] | 2 | GP10 |
| ledPins[2] | 3 | GP9 |
| ledPins[3] | 4 | GP8 |
| ledPins[4] | 5 | GP7 |
| ledPins[5] | 6 | GP6 |
| ledPins[6] | 7 | GP5 |
| ledPins[7] | 8 | GP4 |
| ledPins[8] | A | GP3 |
| ledPins[9] | B | GP2 |
| ledPins[10] | C | GP28 |
| ledPins[11] | D | GP27 |

## Power and grounding
- Common LED cathodes -> Pico GND
- Keypad row pull-up network (`rp1`..`rp4`) -> Pico 3V3

## Assumptions and notes
- The source code uses Arduino-style APIs (`setup()`, `loop()`, `Keypad.h`, `digitalWrite`).
- Pico W pinout is compatible with Pico for GPIO usage in this project.
- Wi-Fi hardware is not used by this firmware.
