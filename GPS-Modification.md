# GPS Modification
As of ESP32 Marauder firmware version 0.11.0, users can modify their Marauder hardware to use external GPS modules. These GPS modules provide location data used for wardriving(planned). The following GPS module was used during testing.

<img src="https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/b52b881b-5dd3-4900-8f88-d09e3fe66d9a" width="400">  

*Teyleten Robot ATGM336H NEO-6M*

## Connections
Connect your GPS module VCC and GND to corresponding VCC and GND on your Marauder. Use the following table as a reference to make the UART connection between your Marauder and GPS module:

| Hardware | TX | RX |
| -------- | -- | -- |
| OG Marauder | IO04 | IO13 |
| Marauder v6 | IO04 | IO13 |
| Marauder Kit | IO04 | IO13 |

Use a piece of strong double sided tape like from 3M to adhere the GPS module and antenna to a spot on the Marauder PCB/Enclosure.  
<img src="https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/26a104dc-784e-497f-ac4d-549ee1f2a831" width="400"> 


## Verifying Successful Installation
You will know if you've successfully installed the GPS module if you see a "GPS" menu item on the main menu of Marauder. You will also see a red or green satellite icon on the far left side of your status bar. If you have not properly installed the GPS module or you used an incompatible GPS module, you will **not** see these two items.
<img src="https://github.com/justcallmekoko/ESP32Marauder/assets/25190487/6823c140-407e-4a21-a16d-903a882f20d7" width="400"> 
