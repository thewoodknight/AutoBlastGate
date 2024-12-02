# AutoBlastGate
Controllers for coordinated blast gate that can open and close via remote push buttons.
Open one gate, then all others close after a delay.

### Hardware List (Per gate)
* [ESP8266 NodeMCU Controller+ L293D board](https://www.aliexpress.com/item/1005006991297846.html)
* [240-500rpm 3v-6v motor](https://www.aliexpress.com/item/1005005474559049.html)
* [200mm T8 lead screw + nut](https://www.aliexpress.com/item/32916461598.html)
* 2x [Limit switches](https://amzn.to/49kIQWi)
* 2x [Bearings](https://amzn.to/4eVeCdx)
* [Coupler (3mm x 8mm)](https://www.aliexpress.com/item/32911705284.html)

### Software
The NodeMCU/ESP8266 boards can be programmed directly thanks to the CP2102 interface, but rather than using Arduino IDE, [ESPHome](https://esphome.io/) allows a lot more interoopability with things like HomeAssistant.

For *my* usage, I'll be using HomeAssistant and NodeRed to coordinate the open/closed states of the gates. However, there will be a version that sets one unit to be the 'coordinator' and the rest to communicate with it maintain the correct open/closed gate states.
