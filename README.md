# Fluke-BE860-series-restoration

Mechanical specifications, sourcing information, and alternatives for those restoring Fluke test equipment that uses the BE860 Battery Eliminator (including Fluke 863, Fluke 865, and Fluke 867B Graphical Multimeters)

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/865-jack-external.jpg" width="500"/>

(Click any image for super hi-rez version)

On the EEVBlog Forum and other places, I've seen many folks asking about getting power
adapters for older Fluke products, specifically the Graphical Multimeters of the following
models:

  - Fluke 863
  - Fluke 865
  - Fluke 867
  - Fluke 867B
  
These are great devices, and I hope they can continue to be restored for a long time to
come.  

These accept a non-standard power plug that originally came attached to the BE860-series
Battery Eliminator, which is no longer manufactured.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/BE860-series-connector-2.jpg" width="500"/>

There are some 3rd party products
out there but they are outrageously priced, and of apparent sub-Fluke-quality standards.
For example, one seen on eBay shows the same part number as a cheap made-in-China power
brick, but with a different connector spliced on.
                      
### Life without a Battery Eliminator

You can still use your device with 6x AA batteries, though this could get expensive.

TODO: Instructions on desktop recharging a Fluke battery.

TODO: Discussion on NiCd vs NiMH batteries and chargers, by model.
IMPORTANT: charging a NiMH battery in a device with a NiCd charger could be dangerous!

## Electrical specifications

12V at 500ma center positive

The underlying power supply should be of Fluke caliber in terms of noise, isolation, etc.
Under no circumstances should one attach a low-end power supply of the sort you can pick
up for $8 or whatever on eBay or numerous sites. If you do, you will get what you deserve.

The internal connection terminates in a 3-pin connector with standard 0.1" spacing, with
pin 1 (square pad on the PCB) connecting to red (positive), pin 2 to green, and pin 3 to
black (negative). The green wire on pin 2 appears to be directly connected to the black
wire.

## Mechanical specifications

(As of this writing, I do not have either a genuine or 3rd-party plug in hand to perform
exact caliper measurements. If you do, please contact me, or file a ticket on this repo.)

### Jack

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/BE860-jack-internal.jpg" width="500"/>

While most devices mount a DC power connector at the outer casing, this one is mounted 
deeper inside, and thus requires a longer extension on the plug, detailed below. The jack
assembly slides out with no fasteners, once the back case and top PCB have been removed.

The internal mount consists of two plastic pieces glued together, and reasonably easy to
separate, revealing inside an ordinary barrel jack connector, with an "EX" logo.

<img src="https://raw.githubusercontent.com/mdubinko/Fluke-BE860-series-restoration/main/photos/BE860-jack-internal-2jpg.jpg" width="500"/>

The jack itself snugly fits a Jameco 71192 connector [1] which is spec'd at
OD 3.5 +/- 0.05mm and ID 1.3 +/- 0.05mm. The Jameco plug is spec'd to have a length of
9.5 +/- 0.1mm, and it leaves a gap of about 2.2mm when it can't be inserted further,
though it can still make reliable contact for at least 2.0mm before hitting the end-stop.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/BE860-jack-fit-jameco.jpg" width="500"/>

[1] https://www.jameco.com/z/G1P639-R-Jameco-Valuepro-Plug-DC-Power-Female-1-3mm-x-3-5mm-with-Strain-Relief-Black_71192.html

### Plug

For reference, I will refer to the parts as follows. This is by no means a standard,
just something made up for the purposes of this document.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/BE860-series-connector.jpg" width="500"/>

    Naming of the parts (not to scale)
    
              |<--------------- plastic sheath --------------->|
                                    ---------------------------+
               ____________________/                           |
     +--------+     (plastic)     .           (plastic)        |
    || barrel |     extension     .            grip            |
     .________+                   .                            |
              +--------------------                            |
                                  |\___________________________|
                                  |
           <-- fits inside device | sticks out of device -->

Based on the earlier observations, the barrel part of the jack--the metal part that makes
physical connection with the charging circuit, is a 3.5mm OD barrel connector,
with an ID of 1.3 or maybe the more common 1.35mm. Aside from the Jameco part, some other
possible parts are:

  - DigiKey CP-PPM-2-35135-B-ND
  - DigiKey CP-PPM-2-35135-BG-ND

The extension is covered with insulating plastic, and has an OD of perhaps 4.5mm.
Anything larger would not fit through the opening in the outer shell of the device.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/865-jack-external-ruler.jpg" width="500"/>

The length of the extension is about twice the length of the barrel. Approximate lengths:

  - Barrel: 9mm
  - Extension: 17mm

Based on caliper measurements, the maximum distance (on a Fluke 865) from the outside
wall of the enclosure to the end-stop is 28.0mm. This accounts for the length of the
barrel + extension. The sharpie line on the internal housing shows the position of
the end stop.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/865-internal-jack-assembly.jpg" width="500"/>

The grip dimensions are not very important, as they will not affect the ability to
insert the plug into the device.

