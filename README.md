# Pico W Keypad-to-LED Controller

A Raspberry Pi Pico W project that reads a 4x4 membrane keypad and controls 12 LEDs using fixed key-to-action mappings.

> Core behavior is preserved from the provided source logic.

## Features
- 4x4 keypad scanning via `Keypad` library.
- 12 independently driven LEDs.
- Group ON/OFF controls for two LED banks:
  - Bank 1 (labels `1..8`) via keys `9` (ON) and `0` (OFF)
  - Bank 2 (labels `A..D`) via keys `*` (ON) and `#` (OFF)
- Compatible GPIO mapping for Raspberry Pi Pico W.

## Repository layout

```text
.
├── CMakeLists.txt
├── include/
├── src/
│   └── main.cpp
└── docs/
    ├── architecture.md
    └── wiring.md
```

## Key mapping summary
- `1..8` -> turn ON corresponding LED 1..8
- `9` -> turn ON LEDs 1..8
- `0` -> turn OFF LEDs 1..8
- `A..D` -> turn ON corresponding LEDs A..D
- `*` -> turn ON LEDs A..D
- `#` -> turn OFF LEDs A..D

## Build/flash for Pico W (Pico SDK flow)

### 1) Prerequisites
- ARM GCC toolchain
- CMake + Ninja/Make
- Pico SDK installed locally

Set SDK path:

```bash
export PICO_SDK_PATH=/absolute/path/to/pico-sdk
```

### 2) Configure and build

```bash
mkdir -p build
cd build
cmake ..
cmake --build .
```

Output UF2 will be generated in `build/`.

### 3) Flash to Pico W
1. Hold **BOOTSEL** while connecting Pico W via USB.
2. Copy generated `.uf2` file to the mounted RPI-RP2 drive.
3. Board reboots and runs firmware.

## Run in Wokwi
1. Create a Wokwi Raspberry Pi Pico project.
2. Paste the supplied `diagram.json` wiring.
3. Use firmware code equivalent to `src/main.cpp` (Arduino-style logic as provided).
4. Start simulation and press keypad keys to observe LED states.

## Real-hardware notes
- Use one 220 Ω resistor in series with each LED anode.
- Tie all LED cathodes to GND.
- Keep keypad row/column wiring identical to `docs/wiring.md`.
- The optional row pull-ups shown in the diagram are connected to 3V3.

## Wi-Fi credential handling
This firmware does **not** use Wi-Fi. If Wi-Fi is added later:
- keep credentials out of source control,
- use a local config header or environment-injected build definitions,
- provide a `config.example` without secrets.
