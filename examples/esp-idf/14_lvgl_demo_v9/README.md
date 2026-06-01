# LVGL Demo v9

Run LVGL v9 demos on a supported display.

## Difficulty

Advanced.

## Hardware Required

- ESP32-P4 board.
- Supported LCD panel.
- PSRAM enabled.

Touch hardware may be required depending on the selected LVGL demo and board
configuration.

## Build and Flash

```bash
cd examples/esp-idf/14_lvgl_demo_v9
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

This example uses LVGL v9 and BSP/display-related managed components. Check
`main/idf_component.yml`, `components/bsp_extra/idf_component.yml`, and
`sdkconfig.defaults` when changing LVGL or display behavior.

## Expected Behavior

The display should initialize and run an LVGL demo.

## Troubleshooting

- Run [13_Displaycolorbar](../13_Displaycolorbar/) first to verify the panel.
- Confirm PSRAM is initialized.
- Check LVGL buffer size and display resolution settings.
- If touch does not work, verify the touch controller and I2C pins separately.
