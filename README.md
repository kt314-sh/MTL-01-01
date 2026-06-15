<div align="center">
<h1>📡 MTL-1: High-Power LoRa Node</h1>
<img src="03-pic/MTL-var.2-b.jpg" alt="Logo" width="70%"> 
  
<div align="left">
  
  # MTL-1
MTL-1 is a LoRa project based on ESP-32 s3 modules and [Ebyete](https://www.ebyte.com/) modules such as E22-xxxM30S, E22p-xxxM30S, E220-xxxM30S, E22-xxxM33S
Designed to work in [MeshCore](https://github.com/meshcore-dev ), [Meshtastic](https://github.com/meshtastic ), as a client and repeater.
 The project is almost fully compatible with Heltec v3, Heltec WSL3.

### MTL-1 is available in three versions

#### Version 1. (not tested)
Support for Li-ion battery. When powered by USB, the DC Up converter is disconnected, and the e22 module receives a voltage of ~4.6V. When powered by the battery, DC Up is activated, and the e22 module receives a voltage of 5v.

#### Version 2
Support for Li-ion battery. When powered by USB, the DC Up converter is activated, and the e22 module receives a voltage of 5v. When powered by the battery, DC Up is activated, and the e22 module receives a voltage of 5v.

#### Version 3
There is no Li-Ion battery support. When powered by USB, the e22 module receives a voltage of ~4.6V.

### Power supply
The main power supply of the MTL-1 is provided via the "USB-C" or "X5" connectors, with a voltage of 5V, the recommended power supply current is 1.5...2A

### Connecting a 3.7V Li-Ion battery (Version 1&2)
- To connect a battery without protection, use the "X6" connector. Maximum battery charge current 1A

- In the case of using a battery with protection, it is necessary to connect the +battery to the "Battery+" connector "X6", and the -battery to the "-" connector "X5".

### Additional IO
Available IO: 2, 3, 4, 5, 6, 7, 19, 20, 38, 39, 40, 41, 42, 45, 46, 47, 48

### Connecting the antenna to IPEX
To use IPEX, the "R18" jumper must be removed

### Connecting an Oled display (SSD1306)
- G	GND
- V	+3.3v (Vcc)
- CL	i2c-SCL
- D	i2c-SDA






For a full description, see the link
https://github.com/vy52am0u/MTL
