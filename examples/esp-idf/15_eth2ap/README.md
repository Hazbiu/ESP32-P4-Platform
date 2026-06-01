# Ethernet To AP

Network example that combines Ethernet and Wi-Fi AP behavior.

## Difficulty

Advanced.

## Hardware Required

- Ethernet-capable ESP32-P4 board or supported Ethernet module.
- Wi-Fi support path.
- Ethernet cable and network.

## Build and Flash

Use an ESP-IDF terminal first. If your editor plugin fails to build this
example, verify the command-line flow before debugging the editor setup.

```bash
cd examples/esp-idf/15_eth2ap
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

Check both Ethernet and Wi-Fi AP settings in `menuconfig`. The correct
Ethernet PHY values depend on the board schematic.

## Troubleshooting

- Bring up [11_ethernetbasic](../11_ethernetbasic/) first.
- Bring up a Wi-Fi example first.
- Check IP address ranges and DHCP behavior.
- Confirm your board supports both required network paths.
