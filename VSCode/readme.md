# platformio.ini

## example 1
```ini
  [common]
  com_port = COM16


  [env:esp32-evb]
  platform = espressif32
  board = esp32-evb
  framework = arduino
  upload_port = ${common.com_port}
  monitor_speed = 230400
  monitor_port = ${common.com_port}

  build_flags =
    -I include
```
## example 2 - Teensy as a keyboard
``` ini
; PlatformIO Project Configuration File
;
;   Build options: build flags, source filter
;   Upload options: custom upload port, speed and extra flags
;   Library options: dependencies, extra library storages
;   Advanced options: extra scripting
;
; Please visit documentation for the other options and examples
; https://docs.platformio.org/page/projectconf.html

[env:teensy35]
platform = teensy
board = teensy35
framework = arduino
build_flags = -DUSB_KEYBOARDONLY -DLAYOUT_GERMAN
; -DUSB_SERIAL_HID
; -D USB_KEYBOARDONLY
```
