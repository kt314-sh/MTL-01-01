<div align="center">
<h1>📡 MTL-1: High-Power LoRa Node</h1>
<img src="03-pic/MTL-var.2-b.jpg" alt="Logo" width="70%"> 
  
<div align="left">
  
  # MTL-1
MTL-1 is a LoRa project based on ESP-32 s3 modules and [Ebyte](https://www.ebyte.com/) modules such as E22-xxxM30S, E22p-xxxM30S, E220-xxxM30S, E22-xxxM33S
Designed to work in [MeshCore](https://github.com/meshcore-dev ), [Meshtastic](https://github.com/meshtastic ), as a client and repeater.
- The project is almost fully compatible with Heltec v3, Heltec WSL3.
- 1A Standalone Linear Li-Ion Battery Charger
- Battery protection lithium-ion/polymer battery
- DC/DC up to 5V
- SMA connector
- GPIO
- 2 button. RESET, BOOT


 The device has proven itself well as a repeater and bridge 868/433
 
 <img src="03-pic/Node-01.jpg" alt="rpt1" width="10%"> <img src="03-pic/bridge-1.jpg" alt="rpt2" width="20%"> <img src="03-pic/bridge-2.jpg" alt="rpt3" width="20%"> 

### MTL-1 is available in three versions

#### Version 1. (not tested)
Support for Li-ion battery. When powered by USB, the DC Up converter is disconnected, and the e22 module receives a voltage of ~4.6V. When powered by the battery, DC Up is activated, and the e22 module receives a voltage of 5v.

<img src="03-pic/var1-01.PNG" alt="ver1T" width="20%"> <img src="03-pic/var1-02.PNG" alt="ver1B" width="20%">

#### Version 2
Support for Li-ion battery. When powered by USB, the DC Up converter is activated, and the e22 module receives a voltage of 5v. When powered by the battery, DC Up is activated, and the e22 module receives a voltage of 5v.

<img src="03-pic/var2-01.PNG" alt="ver2T" width="20%"> <img src="03-pic/var2-02.PNG" alt="ver2B" width="20%">

#### Version 3
There is no Li-Ion battery support. When powered by USB, the e22 module receives a voltage of ~4.6V.

<img src="03-pic/var3-01.PNG" alt="ver3T" width="20%"> <img src="03-pic/var3-02.PNG" alt="ver3B" width="20%">

### Power supply
The main power supply of the MTL-1 is provided via the "USB-C" or "X5" connectors, with a voltage of 5V, the recommended power supply current is 1.5...2A

<img src="03-pic/MTL-Power.jpg" alt="mtl1pwr" width="20%">

### Connecting a 3.7V Li-Ion battery (Version 1&2)
- To connect a battery without protection, use the "X6" connector. Maximum battery charge current 1A

- In the case of using a battery with protection, it is necessary to connect the +battery to the "Battery+" connector "X6", and the -battery to the "-" connector "X5".

<img src="03-pic/MTL-Battery.jpg" alt="mtlbtr" width="20%">

### Additional IO
Available IO: 2, 3, 4, 5, 6, 7, 19, 20, 38, 39, 40, 41, 42, 45, 46, 47, 48

<img src="03-pic/IO2.png" alt="mtlio1" width="20%"> <img src="03-pic/UART.jpg" alt="mtluart" width="20%">

### Connecting the antenna to IPEX
To use IPEX, the "R18" jumper must be removed

<img src="03-pic/MTL-SMA-IPEX.jpg" alt="mtlsmaipex" width="20%"> <img src="03-pic/MTL-SMA-IPEX-2.jpg" alt="mtlsmaipex2" width="20%"> 


### Connecting an Oled display (SSD1306)
- G	GND
- V	+3.3v (Vcc)
- CL	i2c-SCL
- D	i2c-SDA

<img src="03-pic/oled1.png" alt="mtloled1" width="20%">  <img src="03-pic/oled2.png" alt="mtloled2" width="20%">

### Driver CH340

Download driver [CH340.exe](https://www.wch-ic.com/downloads/CH341SER_EXE.html) [CH340.zip](https://www.wch-ic.com/downloads/CH341SER_ZIP.html) or [Github](https://github.com/jayfourjavier/INSTALL-CH340-ON-WINDOWS-11)


### Case

- А good sealed casing made of Plastic sewer pipe with a diameter of 40-50mm
- The rainproof modem box VT-BOX9 with the antenna MOXON

<img src="03-pic/Case-1.jpg" alt="case1" width="16%"> <img src="03-pic/Case-2.jpg" alt="case2" width="29%"> <img src="03-pic/Case-3.jpg" alt="case3" width="20%">


### Repiters in use

<img src="03-pic/RPT-1.jpg" alt="rpt1" width="20%"> <img src="03-pic/RPT-2.jpg" alt="rpt2" width="15%"> <img src="03-pic/RPT-3.jpg" alt="rpt3" width="20%"> <img src="03-pic/RPT-4.jpg" alt="rpt4" width="20%">


### MeshCore SPB
- [MeshCore SPB](https://meshcore.spb.ru)
- [Telegram MeshCore SPB](https://t.me/meshcore_petersburg)

Additional description, see the link
https://github.com/vy52am0u/MTL
