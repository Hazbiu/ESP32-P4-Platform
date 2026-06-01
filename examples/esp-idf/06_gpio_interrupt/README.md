# GPIO Interrupt

GPIO interrupt and debounce example.

This demo is the next step after [05_gpio_io](../05_gpio_io/). It shows how to
handle GPIO edges in an ISR, pass events to a FreeRTOS queue, and process them
in a normal task.

## Difficulty

Beginner to intermediate.

## Hardware Required

- One ESP32-P4 board.
- Button, jumper wire, or other safe 3.3 V input source.

## Default Pin

| Signal | Default GPIO |
| --- | --- |
| Input | GPIO3 |

Change the input GPIO and debounce time in `idf.py menuconfig`.

## Build and Flash

```bash
cd examples/esp-idf/06_gpio_interrupt
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Expected Output

When the input changes level, the monitor prints an event:

```text
gpio=3 level=0 time=1234567 us
gpio=3 level=1 time=1345678 us
```

## What to Reuse

- `gpio_install_isr_service()` and `gpio_isr_handler_add()`.
- `xQueueSendFromISR()` for passing ISR events to a task.
- A simple software debounce pattern.

