# SP63CE LED Controller Configuration and Commands

The SP63CE is an LED controller from Sperll Tech that uses Bluetooth LE for communicating with the BanlanX App. I was able to find some commands by analyzing the communication between the App and the controller via BLE using PacketLogger. All commands are sent in hexadecimal.

Many versions of this controller exist: https://sperll.com/en/index.php?id=116
From what I have found online, the SP63CE is very similar to the SP630E controller (both are PWM/SPI RGB, RGBW, RGBCCT controllers). The controller that I have is connected to an RGB LED strip and a White CCT strip.

## Bluetooth Configuration

The BLE configuration may vary from one device to the other, but here are the details for my specific controller.
Service ID: `ffe0`
Write: `ffe1`

## Control Commands

In my case, the hex commands had to be written to `ffe1`. For my controller model, all commands begin with `53`. All commands should be sent without spaces.

**Power On**

`53 50 A9 01 00 01 83`

**Power Off**

`53 50 C3 01 00 01 E8`

**Dynamic Effect 1: Rainbow**

`53 53 17 01 00 02 3F 3D`

**Pause Effect**

`53 5D 2C 01 00 01 07`

**Effect Direction**

`53 56 13 01 00 01 38`

**Effect Width/Size**

`53 55 EB 01 00 01 4E`

**Effect Speed**

`53 54 CA 01 00 01 E0`
