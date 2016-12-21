# ScreenSaver Mouse Jiggler

Arduino based hardware mouse emulator, preventing computer screen-saver from kicking in
and locking desktop (eg. during forensic investigation).

## How it works

After installation on hardware device (arduino) and plugging it to computer USB port it
registers itself as regular HID mouse. Every few seconds it makes tiny cursor movements,
emulating "user activity" and preventing screen-saver from locking up desktop.

## Requirements (what you will need)

  * Arduino board with USB support (Arduino Leonardo/Nano/Micro/Micro Pro or simillar - those could be bought from different retailers for less than $5)
  * USB Micro-B (male) to USB Type-A (male) connector - becaue Arduino comes with micro USB port (those are commonly used to transfer data between smartphone and computer)
  * Arduino IDE (https://www.arduino.cc/en/Main/Software) - program Arduino device

## Installation


## Considerations


### Reliability


### Forensic footprint