# Wi-Fi Station

Connect an ESP32-P4 setup to an existing Wi-Fi access point.

## Difficulty

Intermediate.

## Hardware Required

- A board or configuration with Wi-Fi support.
- A 2.4 GHz Wi-Fi access point.

Some ESP32-P4 boards require an external or companion Wi-Fi path. Check your
board documentation before using this example.

## Build and Flash

Use an ESP-IDF terminal first. If your editor plugin fails to build this
example, verify the command-line flow before debugging the editor setup.

```bash
cd examples/esp-idf/10_wifistation
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

In `menuconfig`, open **Example Connection Configuration** or
**Example Configuration** and set:

- Wi-Fi SSID.
- Wi-Fi password.
- Maximum retry count, if needed.

## Expected Output

The serial log should show Wi-Fi initialization, connection attempts, and an
IP address after DHCP succeeds.

## Troubleshooting

- Confirm the board has Wi-Fi support.
- Confirm the SSID and password.
- Use a 2.4 GHz network.
- Move the board closer to the access point if connection retries continue.
