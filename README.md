# Woodsat hamradio

Woodsat serves as a LoRa repeater on the 70 cm UHF band in a sun-synchronous low Earth orbit. It listens to short messages (TBD 64 bytes), in which a repeating delay parameter is set, thus allowing the amateur to target a specific geographical area.
Licensed radio amateurs can contact the satellite with a hardware setup that is described below.

Further updates to this document are provided by Tessa Nikander closer to planned launch date (Oct 15th 2021).

## Hardware requirements

### LoRa

You will need:
* Amplifier (optional)
* LoRa hardware with a LoRa-compatible devboard
     * OR, Gnuradio compatible SDR with GR-Lora

LoRa hardware options:
* Raspberry Pi / Nucleo / ESP32 Etc. devboard to connect with a LoRa board
* LoRa boards:
   * Heltec WiFi LoRa 32 (433MHz)
   * TTGO LoRa32 V1 (433MHz)
   * TTGO LoRa32 V2 (433MHz)
   * T-BEAM + OLED (433MHz)
   * FOSSA 1W Ground Station (433MHz)
   * Semtec SX126X
   * Semtec SX127X
* HopeRF RFM69
* STM32WL

LoRa GRC block: https://github.com/rpp0/gr-lora

## Telemetry details

* Frequency:      433-438 MHz
* Bandwidth:      TBD
* Max TX power:   1 W (30 dBm)
* Modulation:     FSK
* Beacon:         TBD
* Protocol:       Detailed protocol specification will be available on this page prior to launch.


## Where is the satellite now?

After launch, the location of the satellite can be tracked here in real time:
https://www.n2yo.com/
