# Woodsat hamradio

Woodsat can be used by radio amateurs, schools, and the public.
Wisa Woodsat is based on Kitsat, the educational satellite stack.

Operation instructions for Woodsat are available in this document.

## Connecting to Woodsat

There are three ways to connect to Woodsat depending on your preferred setup.

1) 433-438 MHz uplink with LoRa
2) 433-438 MHz uplink without LoRa
3) Orbitcon.io - on your own web browser, if you want to test your equipment or you do not have access to radio hardware

# UHF Telecommand uplink / Telemetry downlink / CW beacon

* Frequency: 433-438 MHz
* Bandwidth: 13-50 kHz
* Max TX power: X.Y W (dBm Z.W)
* Modulation: GFSK, deviation X kHz
* Data and symbol rate: XXXX bits/s
* Variable length packets
* Protocol specification: TBD

## Hardware requirements

### LoRa

You will need:
* A YAGI antenna
* Raspberry Pi / Nucleo / Etc. devboard to connect with a LoRa board
* LoRa board:
   * Heltec WiFi LoRa 32 V1 (433MHz & 863-928MHz versions)
   * Heltec WiFi LoRa 32 V2 (433MHz & 863-928MHz versions)
   * TTGO LoRa32 V1 (433MHz & 868-915MHz versions)
   * TTGO LoRa32 V2 (433MHz & 868-915MHz versions)
   * TTGO LoRa32 V2 (Manually swapped SX1267 to SX1278)
   * T-BEAM + OLED (433MHz & 868-915MHz versions)
   * T-BEAM V1.0 + OLED
   * FOSSA 1W Ground Station (433MHz & 868-915MHz versions)
   * ESP32 dev board + SX126X with crystal (Custom build, OLED optional)
   * ESP32 dev board + SX126X with TCXO (Custom build, OLED optional)
   * ESP32 dev board + SX127X (Custom build, OLED optional)
* Semtec SX1276
* HopeRF RFM69
* STM32WL
* Gnuradio with GR-Lora
* Amplifier (optional)

### UHF AX.25

Communicating on 433-438 MHz without LoRa:

* Detailed protocol information will be available on this site near launch.

## Software requirements

### LoRa (SDR)

Please use this GRC block: (GRC)[grc.com]

### Regular communication (SDR)

For pure 435-438 MHz communication, there's the free-to-use Kitsat protocol, which will be available on this site in July 2021.

#### Windows users

Widnows users can use the graphical version of the groundstation. Download `GS_GUI_Installer.msi`, available [here](http://staging.kitsat.fi).

#### *nix users

A CLI-version of the Kitsat protocol is for \*nix-users and can be used with `screen`. Also available [here](http://staging.kitsat.fi) from July 2021.

## How to know where the satellite is flying

The location of the satellite after launch can be tracked ie. on here in real time:
https://www.n2yo.com/
