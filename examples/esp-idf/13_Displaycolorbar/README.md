# Display Color Bar

Display color bars on a supported LCD panel. This is the simplest ESP-IDF
display bring-up example in the repository.

## Difficulty

Intermediate.

## Hardware Required

- ESP32-P4 board.
- Supported LCD panel connected to the expected interface.

## Build and Flash

```bash
cd examples/esp-idf/13_Displaycolorbar
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Expected Behavior

The LCD should initialize and show color bars.

## Troubleshooting

- Confirm the display panel model and interface.
- Confirm PSRAM is enabled when the panel path needs it.
- Check backlight control if logs look correct but the screen is dark.
- Verify reset, power, and panel initialization settings.
