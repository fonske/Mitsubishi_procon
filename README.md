# Mitsubishi_procon
Modbus RTU communication with ESP32/ESP32S3 and ttl to rs485 module, to use in home assistant / esphome for Mitsubishi Procon A1M mini

# Platforms
Currently supported ESP32 platforms.
By default Lilygo T7-S3 ESP32S3 is used. If you want to use ESP32 (MH-ET-LIVE), edit file `esphome/procon.yaml`, comment out board-esp32s3 include and uncomment board-esp32 include file.

```
packages:
  remote_package:
    url: https://github.com/fonske/Mitsubishi_procon
    ref: main
    files: 
      - esphome/.procon.base.yaml
      - esphome/labels/.procon-labels-en.yaml
      # - esphome/labels/.procon-labels-nl.yaml
      # - esphome/boards/board-esp32.yaml
      - esphome/boards/board-esp32S3.yaml

## for developing/testing, uncomment local includes and comment out remote_package part.
## packages:
#   substitutions: !include labels/.procon-labels-en.yaml
#   device_base1: !include .procon.base.yaml
#   device_base2: !include boards/board-esp32.yaml
```

# Translations
Currently supported languages are en, nl.
In order to change language, edit file `esphome/procon-mitsubishi.yaml`, and change include file (esphome-/.brink-labels-<language>.yaml)

## Contact
Contact me: alphonsuijtdehaag at gmail dot com, if you are interested in a PCB with a ESP32 (mh-et-live or lilygo esp32s3-T7) and XY-017 ttl to rs485 mounted on with 3d printed housing.
See: /pictures
