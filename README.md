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

![arduino-micro-pro](https://raw.githubusercontent.com/nshadov/screensaver-mouse-jiggler/master/docs/img/arduino-1.jpg)
![arduino-usb](https://raw.githubusercontent.com/nshadov/screensaver-mouse-jiggler/master/docs/img/arduino-2.jpg)

## Installation


## Considerations

### Exposed Electronics

Touching exposed electronics (arduino) with naked hands could damage it. Consider putting it in thermal insulation - this should help with ESD.

![arduino-esd](https://raw.githubusercontent.com/nshadov/screensaver-mouse-jiggler/master/docs/img/arduino-3.jpg)

### Reliability


### Forensic footprint