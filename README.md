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

  - Download and install Arduino IDE from their website (https://www.arduino.cc/en/Main/Software).
  - Connect your Arduino board (via onboard micro USB port) to your computer USB port.
  - Open Arduino IDE and open project ```mouse_jiggler.ino``` file from this repository.
  - In Arduino IDE choose device type (```TOOLS > Board > Arduno Micro``` or similar) and port where programmer is connected to (```TOOLS > Port > ...```).
  - Upload your program to Arduino device (right pointing arrow, next to "tick" mark).

## Considerations

  * When plugged in, your Arduino device will be recognized as keyboard & mouse.
  * Mouse cursor should "jiggle" every few seconds, simulating user moving his/her mouse.

### Exposed Electronics

Touching exposed electronics (arduino) with naked hands could damage it. Consider putting it in thermal insulation - this should help with ESD.

![arduino-esd](https://raw.githubusercontent.com/nshadov/screensaver-mouse-jiggler/master/docs/img/arduino-3.jpg)

### Reliability

We've battle tested it during our internal investigations on Mac OSX. Additionally development stability tests were performed on Debian based Linux distro.

In both cases, it's activation was apparent few seconds after insertion and ScreenSaver hasn't kicked in for more than 48h (weekend memory acquisition).

I am not aware of any running time limitation but I cannot guarantee it.

### Forensic footprint

Device acts as normal HID device (usb mouse) and according system journals are updated with entry of inserting USB device. No other files are created/modified except using already installed USB HID drivers.
