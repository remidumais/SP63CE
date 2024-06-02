# SP63CE LED Controller Configuration and Commands

The SP63CE is an LED controller from Sperll Tech that uses Bluetooth LE for communicating with the BanlanX App. All commands are sent in hexidecimal.
Many versions of this controller exist: https://sperll.com/en/index.php?id=116

## Bluetooth Configuration

The BLE configuration may vary from one device to the other, but here are the details for my controller.
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
