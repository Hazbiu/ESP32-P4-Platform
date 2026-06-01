# I2S Codec

Audio codec example using I2S. It can run in music playback mode or echo mode,
depending on configuration.

## Difficulty

Intermediate.

## Hardware Required

- ESP32-P4 board with a supported audio codec path.
- Speaker or headphones for playback mode.
- Microphone input for echo mode, if used.

## Build and Flash

```bash
cd examples/esp-idf/12_I2SCodec
idf.py set-target esp32p4
idf.py menuconfig
idf.py build
idf.py -p PORT flash monitor
```

## Configuration

In **Example Configuration**, check:

- Mode: music or echo.
- Microphone gain.
- Voice volume.
- BSP support option.

## Expected Behavior

- Music mode plays the bundled `canon.pcm` sample.
- Echo mode routes microphone input through the codec path.

## Troubleshooting

- Confirm codec power, clock, I2C control bus, and I2S pins.
- Start with a moderate volume.
- If there is no sound, check whether the selected board path matches your
  hardware.
