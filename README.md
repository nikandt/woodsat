# Woodsat hamradio

Woodsat can be used by radio amateurs, schools, and the public.
Wisa Woodsat is based on Kitsat, educational satellite stack.

Operation instructions for Woodsat are available in this document.

## Connecting to Woodsat

You can communicate with Woodsat using minimal gear described below.
You can send commands to it, relay APRS messages, and even do something fun.

There are three ways to connect to Woodsat.

1) Use your own hamradio gear with LoRa
2) Use somebody else's hamradio gear without LoRa
3) Orbitcon.io - on your own web browser, if you want to check your ham equipment

## Hardware requirements

* Transceiver (preferably SDR)
* YAGI antenna
* LoRa hardware
* Raspberry Pi / Nucleo / Etc. to connect with LoRa

## Software requirements

### LoRa (SDR)

Please use this GRC block: (GRC)[grc.com]

### Regular communication (SDR)

For pure 435-438 MHz communication, there's the free-to-use Kitsat protocol.

#### Windows users

Widnows users can use the graphical version of the groundstation. Download `GS_GUI_Installer.msi`, available [here](http://staging.kitsat.fi).

#### *nix users

A CLI-version of the Kitsat protocol is for \*nix-users and can be used with `screen`. Also available [here](http://staging.kitsat.fi) from July 2021.
