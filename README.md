Modbus RTU communication with ESP32/ESP32S3 and ttl to rs485 module, to use in home assistant / esphome for Mitsubishi Procon A1M mini

# Platforms
Currently supported ESP32 platforms.
By default ESP32 (MH-ET-LIVE) is used. If you want to use Lilygo T7-S3 ESP32S3, edit the line files: [ ]
Newer ESP configurations will be added and files updated.

```
packages:
  remote_package:
    url: https://github.com/fonske/Mitsubishi_procon
    ref: main
    refresh: 0s
    files: [ esphome/labels/.procon-labels-en.yaml, 
             esphome/.procon.base.yaml, 
             esphome/boards/board-esp32.yaml 
           ]
      ## Language Packs:
      # esphome/labels/.procon-labels-en.yaml
      # esphome/labels/.procon-labels-nl.yaml
      ## Base:
      # esphome/.procon.base.yaml
      ## Boards:
      # esphome/boards/board-esp32.yaml
      # esphome/boards/board-esp32S3.yaml
      # esphome/boards/board-m5stack-atom.yaml
      ###
      ## Zone 2, If you have 2 zones on the heatpump enable this:
      # esphome/.procon.zone2.yaml
      ##
      ## EASTRON 3ph SDM, If you have a 3phase Eastron kWh meter on the heatpump enable this:
      # esphome/.procon.sdm.yaml
      ## set parity to none on the kWh meter. Baudrate to 9600
      ## FINDER 1ph 7E 64 8 230 0210. If you have 2 of these kWh meters on the heatpump enable this:
      # esphome/.procon.finder.yaml
      ## set parity to none on the kWh meter. Baudrate to 9600
      ###
```

# Translations
Currently supported languages are en, nl.
In order to change language, edit the line files: `esphome/procon.yaml`

