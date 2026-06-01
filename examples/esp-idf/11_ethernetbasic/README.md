# Ethernet Basic

Bring up Ethernet, wait for link, and obtain an IP address.

## Difficulty

Intermediate.

## Hardware Required

- ESP32-P4 board with Ethernet support, or a supported external Ethernet
  module.
- Ethernet cable and network with DHCP.

## Build and Flash

```bash
cd examples/esp-idf/11_ethernetbasic
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

Check **Example Configuration** and the Ethernet PHY settings:

- Internal or SPI Ethernet mode.
- PHY model.
- PHY address.
- MDC/MDIO GPIOs.
- Reset GPIO.
- Clock mode.

The right values depend on the board schematic.

## Expected Output

The log should show Ethernet driver initialization, link up, and an IP address.

## Troubleshooting

- Confirm your board actually has Ethernet hardware.
- Check cable, switch, and DHCP server.
- Verify PHY address and reset GPIO.
- If link never comes up, check clock mode and PHY power.
