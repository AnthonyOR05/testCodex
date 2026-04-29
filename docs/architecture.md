# Architecture

## Firmware style
The provided firmware is Arduino-style C++ logic targeting RP2040 GPIO behavior:
- `setup()` initializes all configured LED GPIO pins as outputs and sets them LOW.
- `loop()` scans keypad input and maps pressed keys to LED actions.

## Module breakdown

### `src/main.cpp`
Single-module implementation containing:
1. **Static configuration**
   - `LEDS`, `ROWS`, `COLS`
   - Key map matrix `keys[4][4]`
   - Pin maps: `ledPins`, `rowPins`, `colPins`
2. **Input device initialization**
   - `Keypad keypad = Keypad(...)`
3. **Runtime behavior**
   - `setup()` output initialization
   - `loop()` event polling + action dispatch via `switch`

## Behavioral mapping
- Numeric keys `1..8`: set individual blue LEDs ON.
- `9`: set LEDs 1..8 ON.
- `0`: set LEDs 1..8 OFF.
- `A..D`: set individual red LEDs ON.
- `*`: set LEDs A..D ON.
- `#`: set LEDs A..D OFF.

No debounce/filtering besides `delay(10)` loop pacing.

## Suggested repository structure (C/C++ Pico-oriented)
- `src/` firmware sources (`main.cpp`)
- `include/` project headers (reserved for growth)
- `docs/` hardware and architecture docs
- `CMakeLists.txt` build entrypoint
- `README.md` quick start and usage

This keeps logic unchanged while making the project maintainable.
