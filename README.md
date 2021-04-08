# Woodsat hamradio

Woodsat can be used by radio amateurs, schools, and the public.
Wisa Woodsat is based on Kitsat, educational satellite stack.

Operation instructions for Woodsat are available in this document.

## Connecting to Woodsat

You can communicate with Woodsat using minimal gear described below.
You can send commands to it, and relay APRS messages.

There are three ways to connect to Woodsat.

1) Use your own hamradio gear with LoRa
2) Use somebody else's hamradio gear without LoRa
3) Orbitcon.io - on your own web browser, if you want to test your ham equipment

## Hardware requirements

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

## How to know where the satellite is

Before the satellite is launched, some orbit parameters are calculated from the satellite within the rocket.
After that, the parameters get updated.
They will look like this:

????

## Software requirements

### LoRa (SDR)

Please use this GRC block: (GRC)[grc.com]

### Regular communication (SDR)

For pure 435-438 MHz communication, there's the free-to-use Kitsat protocol.

#### Windows users

Widnows users can use the graphical version of the groundstation. Download `GS_GUI_Installer.msi`, available [here](http://staging.kitsat.fi).

#### *nix users

A CLI-version of the Kitsat protocol is for \*nix-users and can be used with `screen`. Also available [here](http://staging.kitsat.fi) from July 2021.
