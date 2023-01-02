# BAE 146 Control Panel

![box_2023-Jan-02_02-31-33AM-000_CustomizedView2868195922](https://user-images.githubusercontent.com/131580/210193589-2818c8e0-bbcb-4c62-88e0-2b58e8e6ed8f.jpg)

A design & build of a replica control panel for a BAE 146 aircraft, for use with flight simulators (e.g. MSFS 2020).


## Acknowledgements

I owe a lot of thanks to the time and effort `Heli Mech` has put into his videos as part of the [737diysim project](https://www.737diysim.com/). **I recommend anyone interested in building this control panel to first watch his [Boeing 737 AutoPilot Panel (MCP)](https://www.youtube.com/watch?v=o9EGCjD7V-M) video**. I learnt a lot from his builds, and used a number of similar approaches & techniques on this design of my own.




## Model Files
- [Complete Fusion 360 model](https://github.com/hcooper/bae-146-control-panel/releases)
- [STL files for 3D printing](https://www.printables.com/model/354370)


## Construction
The overall design screws together quite simply.

Each panel consists of a top & bottom part. The top part includes the text, and screws into the lower part. The lower part conceals any extra fixtures needed to mount components, and then screws into the support frame.

The two part design also helps make the two-tone look. I printed the top panels & boxes in dark grey, and the bottom panels in light grey.

![2023-01-01 20_47_19-Autodesk Fusion 360 (Personal - Not for Commercial Use)](https://user-images.githubusercontent.com/131580/210195905-39420ff4-44f5-4ab4-ac07-d8619e67c3cf.png)

Each panel is standalone, so can be built independently from each other. This helps expand the unit over time. The first panel I built was the autopilot. Despite it having a lot of wiring once complete, there is only one type of components to install (the KD2-22 switches) which clip into place easily. Once you've wired one it's just a case of repeating the pattern.

<img src="https://user-images.githubusercontent.com/131580/210202964-14ba0a3f-5f6b-4b8c-a14b-633ff269510b.jpg" width=600px align="left"><img src="https://user-images.githubusercontent.com/131580/210202983-4d1bb7b5-dd35-442d-9e9b-5ec85d93d15a.jpg" width=600px>

## Parts
### Radio Panel & Alarms

||||
|-|-|-|
|Alarm Buttons	| [PB26-13M Square 15*15mm With LED SPDT Switch](https://www.aliexpress.us/item/2251832813241589.html) |	1x red, 1x yellow	|
|FD Bars Switch	| [SPDT Toggle Switch](https://www.adafruit.com/product/3221)|	1x	|
|Radio Mode Selector Switch	|[Taiss 3pcs Rotary Switch RS26 1P12T](https://www.amazon.com/dp/B074WMC9C8?ref_=pe_386300_442746000_DDT_E_DDE_dt_1&th=1) |	1x	|
|Frequency Swap Button|[LED Illuminated Switch Momentary Push Button Tactile SPST](https://www.ebay.co.uk/itm/165153295027)|1x|
|Tuning Knob & Power Button|[Dual Encoder Kit w/switch](https://www.propwashsim.com/store/dual-encoder-kit)|1x dual rotary encoded|
|NAV/COM Switch|[Mini Panel Mount DPDT Toggle Switch](https://www.adafruit.com/product/3220)|1x DP|
|LEDs|[Diffused 3mm LED](https://www.adafruit.com/product/4202)|1x red, 1x green|
|LCD Display|[RGB backlight LCD 16x2](https://www.adafruit.com/product/399)|1x|


### Autopilot Panel
||||
|-|-|-|
|Buttons with LED|[KD2-22 Illuminated Non Locking Push Button Switch](https://www.amazon.com/gp/product/B07CXN14QV/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)|x12|

### Heading Panel
||||
|-|-|-|
|7 Segment LED Display|[7 Segment LED](https://www.propwashsim.com/store/7segled)|x2 3 digits white|
|NAV selector|*same as radio mode selector*|1x|
|Course & Heading Selectors|rotary encoder|3x|

### Altitude Panel
||||
|-|-|-|
|Button with LED|*same as autopilot panel*|x1|
|7 Segment LED Display|[7 Segment LED](https://www.propwashsim.com/store/7segled)|x1 5 digits white|
|Altitude selector|rotary encoder|1x|




### Other parts

- Screws: I started off with a mixed box like this: https://www.amazon.com/gp/product/B076ZDXK1W
  - the build uses entirely M3 screws (except for M4s to mount the Arduino Mega).
  - M3 4mm countersunk attach the top panels to the bottom panels.
  - M3 6mm rounded-head attach the bottom panel to the support frames.
  - M3 4mm standoff screws mount the LCD & LED displays
 - Paint pen - the raised lettering is printed in the same grey as the rest of the top plate, then delicately gone over with a white paint pen. You'll want to practice this a little at first, it's easy to flood the lettering with too much paint.
 - Arduino Mega - in order to maintain high levels of compatibility mobiflight only supports a limited set of arduino models.
- Wires - nice flexible wires that are easy to route in bundles.	
 - Heat shrink - all solder joints are also heat shrinked for avoid shorts later
 - protoboboard	https://www.amazon.com/gp/product/B07DRG2LN2/ KEYESTUDIO Proto Shield for Arduino Mega
 - heat set threaded nuts	https://www.amazon.com/dp/B093357W32/ref=dp_iou_view_item?ie=UTF8&psc=1
 - led button cover, taken from 737diysim project https://a360.co/3cJWwxx



## Wiring

Everything is wired to a protoboard that sits on top of the Arduino. This means the Arduino can be swapped out easily, without having to remove any wires.

A single common ground wire is connected to every component.

The current design consumes almost every pin on an Arduino Mega. This is my arduino [wiring schematic](https://github.com/hcooper/bae-146-control-panel/files/10330010/bae146.build.-.Wiring.Schematic.pdf). Adding an extra Arduino in future should only require a little internal redesign. MobiFlight is able to control multiple Arduinos simultaneously.




## Software

Mobiflight takes care of all the configuration and communication with the flightsim.

TODO: upload mobiflight configs that do clever NAV/COM stuff.



## Gallery

Model:
![box_2023-Jan-02_03-36-28AM-000_CustomizedView22849700086](https://user-images.githubusercontent.com/131580/210194112-c9b5376b-5c2c-44ac-94b8-7276cb43d5f8.jpg)

Final build:
![PXL_20220816_222251135 MP](https://user-images.githubusercontent.com/131580/210194150-04224985-87d7-4500-a0fc-10ae9fdd6f5d.jpg)

More photos: https://photos.app.goo.gl/MFjjrHNgJydS1jSQ8
