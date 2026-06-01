# UART Loopback

Small UART example that sends text from TX and reads it back on RX.

## Difficulty

Beginner to intermediate.

## Hardware Required

- One ESP32-P4 board.
- One jumper wire between the configured TX and RX pins.

## Default Pins

| Signal | Default GPIO |
| --- | --- |
| TX | GPIO43 |
| RX | GPIO44 |

Change these in `idf.py menuconfig` if the pins conflict with your board.

## Build and Flash

```bash
cd examples/esp-idf/07_uart_loopback
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Expected Output

With TX connected to RX:

```text
received 33 bytes: hello from esp32-p4 uart loopback
```

Without the jumper, the example prints a warning.

## What to Reuse

- `uart_driver_install()`
- `uart_param_config()`
- `uart_set_pin()`
- `uart_write_bytes()` and `uart_read_bytes()`
