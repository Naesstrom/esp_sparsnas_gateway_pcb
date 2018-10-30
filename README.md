# PCB for ESP Sparsnas Gateway
In the early days of mankind it was possible to tap into the signals from IKEA's sparsnär energy meter and send them to [Home-Assistant](http://www.home-assistant.io) using a simple docker image from [Tubalainen](https://github.com/tubalainen/sparsnas_decoder)

But then the age of hassbian passed and mankind ventured onwards to hassos and thus dockers was no longer a viable option _(sad face emoji)_

But the dark ages lasted only a moment since the enlightened [bphermansson](https://github.com/bphermansson) created his code for the [ESP_Sparsnas_gateway](https://github.com/bphermansson/EspSparsnasGateway), a slightly magical thingymajig that instead of using a USB-Dongle use a ESP8266 and a reciever to send the measured values by mqtt do your chosen destination... just like magic!

# So why do I need a PCB?
Well you don't _need_ a pcb... but then again there are a lot of things that we don't _need_ but the geeky heart want its fiddly little thingies to show off.
If you don't want a PCB here's bphermansson's scheme for connecting all the cables!
![schematic](https://github.com/bphermansson/EspSparsnasGateway/blob/master/EspSparsnasGateway_schem_Nodemcu.png)
Right... so now that we've concluded that you don't **need** a PCB but rather that you really **want** one to make it easier...

# Ok Ok... I'm listening, go on!
Just order the PCB's from any online shop of your choosing. Personally I prefer Seeed studio and you can even find the uploaded files by clicking here so just **click, click, click** and get your own PCB!
You need a few moore parts to tough:
* PCB _(doh)_
* [NodeMCU v3](https://www.banggood.com/V3-NodeMcu-Lua-WIFI-Development-Board-p-992733.html?p=OT281219548009201802) _(bigger footprint then v2)_
* Adafruit RFM69HCW Transceiver Radio Breakout 
* [100nF Capacitor](https://www.banggood.com/100pcs-0_1uF-104-50V-100nF-104M-Multilayer-Ceramic-Capacitor-p-1094956.html?p=OT281219548009201802) _(C1)_
* 1000uF Capacitor _(C2)_ **Must have 3.5mm legdistance**
* [100uH Induktor](https://www.banggood.com/14W-1UH-1MH-120pcs-12-Values-0307-Color-Ring-Inductor-Pack-Color-Code-Inductor-10pcs-Each-Value-p-1174702.html?p=OT281219548009201802) _(L1)_
* [Power Plug](https://www.banggood.com/50pcs-DC-005-3Pin-Black-DC-Power-Jack-Socket-Connector-5_52_1mm-p-1127042.html?p=OT281219548009201802)
* [Female SMA for PCB mount](https://www.banggood.com/10Pcs-SMA-Female-Solder-Edge-PCB-Mount-Straight-RF-Connector-Plug-p-1076487.html?p=OT281219548009201802) _(or just a 8cm cable as antenna)_
* 868MHz SMA Antenna

# Assembly
Ok, time to get the party started... this is how the PCB looks
![clean pcb](https://github.com/Naesstrom/esp_sparsnas_gateway_pcb/blob/master/images/pcb_clear.JPG)

Now add all the components and it should look something like this:
![clean pcb](https://github.com/Naesstrom/esp_sparsnas_gateway_pcb/blob/master/images/pcb_components.JPG)

And then just plug in the ESP and the radiocard, plug it into your computer and flash the firmware according to the instructions.
![clean pcb](https://github.com/Naesstrom/esp_sparsnas_gateway_pcb/blob/master/images/pcb_complete.JPG)

Now just flash the firmware according to bphermansson's instructions and you're all set!
