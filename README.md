
This script will establish Serial to MIDI bridge.
It will be useful with micro controller boards such as Arduino, ESP32.

I made this since useful [Hairless MIDI Serial bridge](https://github.com/projectgus/hairless-midiserial) program stopped working with OS X Catalina.

It processes most of MIDI messages. Latency can be adjusted. I could archive very low latency (probably less than 5ms) so far.

## Quickstart
```
$ python3 serialmidi.py --serial_name=/dev/cu.SLAB_USBtoUART --midi_in_name="IAC Bus 1" --midi_out_name="IAC Bus 2"
```
The script will put a list of device names. Use the listed name for --midi_in_name and midi_out_name.

### Requirements

This script needs [python-rtmidi](https://pypi.org/project/python-rtmidi/), [PySerial](https://pypi.org/project/pyserial/) and Python 3.

### Tested environment
- I only tested with OS X Catalina with ESP32 board. I'm not using any OS-specific functions so probably it will work on other systems, as long as RTMIDI supports it.

### Other notes
- I made it for my ESP32 based synthesizer, so I tested MIDI IN a lot, but MIDI OUT. MIDI OUT message processing might have some bugs. Please let me know if you find it.


