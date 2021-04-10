# Woodsat hamradio

This document guides you to getting started with Woodsat.
Further updates to this document are provided by Tessa Nikander closer to planned launch date (Oct 15th 2021).

## Setup

There are three ways to connect to Woodsat depending on your preferred setup.

1) 433-438 MHz uplink with LoRa
2) 433-438 MHz uplink without LoRa
3) Orbitcon.io - on your web browser, if you want to test your equipment or if you do not have access to radio hardware

## UHF Telecommand uplink / Telemetry downlink / CW beacon

* Frequency: 433-438 MHz
* Bandwidth: 13-50 kHz
* Max TX power: 1.0 W (dBm 30.0)
* Modulation: GFSK, deviation 13 kHz
* Data and symbol rate: 9600 bits/s
* Protocol specification: see [Kitsat protocol](#uhf-ax25--kitsat-protocol) 

## Hardware requirements

### LoRa

You will need:
* Amplifier (optional)
* LoRa hardware with a LoRa-compatible devboard
     * OR, Gnuradio with GR-Lora

LoRa hardware options:
* Raspberry Pi / Nucleo / Etc. devboard to connect with a LoRa board
* LoRa boards:
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

### UHF AX.25 / Kitsat Protocol

Communicating on 433-438 MHz without LoRa:

*Detailed protocol specifications and operation instructions will be available on this page prior to launch.

Kitsat protocol is free to use.

Designed TX frame:

| Beacon | Target          | Origin          | Command ID      | Data length     |
|--------|-----------------|-----------------|-----------------|-----------------|
|        | 0 0 0 0 0 0 0 1 | 0 0 0 0 0 0 1 0 | 0 0 0 0 0 1 0 0 | 1 0 1 1 1 0 1 1 |
|        |                 |                 |                 |                 |
|        |                 |                 |                 |                 |

| Data (53 bytes) | FNV                                                                |
|-----------------|--------------------------------------------------------------------|
|                 | 0 0 1 1 0 1 0 1  1 0 0 0 0 1 1 0  0 0 0 0 0 1 1 0  1 0 0 1 0 0 0 0 |
|                 |                                                                    |
|                 |                                                                    | 

## Software requirements

### LoRa (SDR)

Please use this GRC block with LoRa: https://github.com/rpp0/gr-lora

### Regular communication (SDR)

Please see section [Kitsat protocol](#uhf-ax25--kitsat-protocol) above.

#### Windows users

Widnows users can use the graphical version of the groundstation. Download `GS_GUI_Installer.msi`, available [here](http://staging.kitsat.fi).

#### *nix users

A CLI-version of the Kitsat protocol is for \*nix-users and can be used with `screen`. Also available [here](http://staging.kitsat.fi) from July 2021.

## How to know where the satellite is flying

The location of the satellite after launch can be tracked ie. on here in real time:
https://www.n2yo.com/
