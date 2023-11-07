# Mitsubishi_procon
Modbus RTU communication with ESP32/ESP32S3 and ttl to rs485 module, to use in home assistant / esphome for Mitsubishi Procon A1M mini

# Platforms
Currently supported ESP32 platforms.
By default ESP32 (MH-ET-LIVE) is used. If you want to use Lilygo T7-S3 ESP32S3, edit file esphome/procon.yaml`, uncomment board-esp32 include and comment out board-esp32S3 include file.
Newer ESP configurations will be added and files updated.

```
packages:
  remote_package:
    url: https://github.com/fonske/Mitsubishi_procon
    ref: main
      # Language Packs:
      - esphome/labels/.procon-labels-en.yaml
      #- esphome/labels/.procon-labels-nl.yaml
      # Base:
      - esphome/.procon.base.yaml
      # Boards:
      - esphome/boards/board-esp32.yaml
      #- esphome/boards/board-esp32S3.yaml
      #- esphome/boards/board-m5stack-atom.yaml
      ###
      ## Zone 2, If you have 2 zones on the heatpump enable this:
      #- esphome/.procon.zone2.yaml

## for developing/testing, uncomment local includes and comment out remote_package part.
#packages:
#  substitutions: !include labels/.procon-labels-nl.yaml
#  device_base1: !include .procon.base.yaml
#  device_base2: !include boards/board-esp32.yaml
#  device_base2: !include boards/board-esp32S3.yaml
```

# Translations
Currently supported languages are en, nl.
In order to change language, edit file `esphome/procon.yaml`, and change include file (esphome/labels/.procon-labels-<language>.yaml)

## Contact
Contact me: alphonsuijtdehaag at gmail dot com, if you are interested in a PCB with an ESP32 (mh-et-live or lilygo esp32s3-T7) and XY-017 ttl to rs485 mounted on with 3d printed housing.
