# SDMMC

Mount and test an SD card over the SDMMC interface.

## Difficulty

Intermediate.

## Hardware Required

- ESP32-P4 board with SD card slot or wired SD card module.
- SD card.

## Build and Flash

```bash
cd examples/esp-idf/09_sdmmc
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

In **SD/MMC Example Configuration**, check:

- Bus width: 4-line or 1-line mode.
- CMD, CLK, D0, D1, D2, D3 GPIOs.
- Format options.
- SD power control options.

Do not enable format options unless you are willing to erase the card.

## Expected Output

The example should mount the card, print card information, write a file, read
it back, and unmount the card.

## Troubleshooting

- Try 1-line mode when wiring is uncertain.
- Check card detect and power wiring if your board uses them.
- Use a known-good SD card formatted as FAT.
- Keep SDMMC wires short when using an external module.
