# platformio.ini

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
