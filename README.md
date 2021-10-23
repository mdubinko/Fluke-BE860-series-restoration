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

If you have a Fluke battery, it can charge on a standard charger that supports 6S NiMH.
(Have not verified on a NiCd battery, but these are more forgiving in charging, so it
would probably work.)

TODO: Discussion on NiCd vs NiMH batteries and chargers, by model.
IMPORTANT: charging a NiMH battery in a device built for charging NiCd could be dangerous!

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

### Jack

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/BE860-jack-internal.jpg" width="500"/>

While most devices mount a DC power connector at the outer casing, this one is mounted 
deeper inside, and thus requires a longer extension on the plug, detailed below. With
the case open, the jack assembly slides out with no fasteners, once the back case and
top PCB have been moved out of the way.

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

Measured dimensions from an EEVBlog thread given in references:

  - Barrel inner diameter: between 1.2mm and 1.38mm
  - Barrel outer diameter: 3.46mm (3.5mm acceptable)
  - Barrel length: 8.3mm
  - Extension outer diameter: 4.9mm
  - Extension length: 20mm

Aside from the Jameco part, some other possible parts for the barrel connector are:

  - DigiKey CP-PPM-2-35135-B-ND
  - DigiKey CP-PPM-2-35135-BG-ND

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/865-jack-external-ruler.jpg" width="500"/>

Based on caliper measurements, the maximum distance (on a Fluke 865) from the outside
wall of the enclosure to the end-stop is 28.0mm. This accounts for the length of the
barrel + extension, with the plug snug against the outer case.
The sharpie line on the internal housing shows the position of the end stop.

<img src="https://github.com/mdubinko/Fluke-BE860-series-restoration/raw/main/photos/865-internal-jack-assembly.jpg" width="500"/>

The grip dimensions are not particularly important, as they will not affect the ability
to insert the plug into the device.

## Construction options

Some various option to power a restored device.

### Constructing a plug

One option is to take a normal 3.5mm barrel connector, like Jameco 71192 or numerous
others, and attach a longer length of barrel connector, like DigiKey CP-PPM-2-35135-B-ND,
then applying heat shrink, resulting in a plug that can be attached to a quality 12V
source and used as a replacement for the BE860.

The latter connector has a center-pin solder cup about 1.4mm in diameter, and can be
gently swaged into the end of a ID 1.3 or 1.35mm connector with a vise and rubber mallet.

The lower center conductor might start to push out the back, and so might require physical
support while convincing the two pieces together. And the black plastic insulating ring
might break off, in which case some JB-Weld will do the trick.
(Yes, this is non-conductive)

This will leave the top outer connection floating, so some conductive copper tape and
maybe a little solder will complete the connection. Cover the assembly with heat-shrink.

<img src="https://raw.githubusercontent.com/mdubinko/Fluke-BE860-series-restoration/main/photos/Homemade_Fluke_860_series.jpg" width="500"/>


###  Other options to consider

  - Mount a more convenient barrel jack right against the inner wall of the enclosure
  - Bypass the charging port and get 12V into the 3-pin DC connector some other way
    - (Depending on the model, this may not adequately/safely charge NiMH internal batteries)
  - Get 9V into the battery posts for the AA batteries
  - Get 7.2V into the pins used to connect the internal battery

I have not tried any of these. Do so at your own risk (but do report back on what works)

## References

  - https://www.eevblog.com/forum/testgear/fluke-scopemeter-860-charger-battery-eliminator/ 
  - https://www.eevblog.com/forum/testgear/fluke-867b-good-or-obsolete/
  - https://www.eevblog.com/forum/repair/fluke-867-863-865-or-867b-charging-adapter-connector-physical-dimensions/

