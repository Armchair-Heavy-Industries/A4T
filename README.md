[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

# A4T: [A]nother [4]010 [T]oolhead
An Armchair toolhead from: [![ko-fi](docs/images/Ko-fi_smol.png)](https://ko-fi.com/O5O5OCC0K) [DW-Tas](https://github.com/DW-Tas)

[![Join me on Discord](https://discord.com/api/guilds/1029426383614648421/widget.png?style=banner2)](https://discord.gg/armchairengineeringsux)

<img src='docs/images/A4T_render.png' width=800 />


<br/> 
After the last year or two looking after Xol and transforming it into Xol Toolhead, I thought it was about time I tried to see if I could design something from scratch. The result is A4T: [A]nother [4]010 [T]oolhead <br/><br/>

A4T is built around the following constraints:
* Dual 4010 blower fans for part cooling
* HF and some UHF hotends (originally designed around Dragon HF with an extender).
* 2510 hotend cooling with well-directed hotend cooling airflow. (Can't beat the amazing 5v Delta 2510)
* ***Easy Assembly***
* Custom Wrist Watch BMG mod with Sherpa-Mini spacing. Also works with Sherpa-Mini. (Some WWG2 and oribter options now too)
* Neopixel LEDs with good part lighting from in front of the nozzle.
* Built for Xol-Carriage - can work with Voron Tap / Standard Voron CW2 carriage.

## Pre-requisites
A printer that fits either Xol carriage, or a standard voron CW2 or Tap carriage.<br/>
<br/>
To avoid build plate area loss:
- X/Y gantry joints that are within the same size as standard Voron 2.4 or Trident X/Y joints.
- Slimmer than stock idlers (see warning below) 

See Voron Design instructions to install TAP.<br/>
`If using tap, highly recommended to replace M3x50 SHCS with button head screws for better build plate clearance.`<br/>

> [!NOTE] 
> ### Notes for Xol-Carriage<br/>
> * Xol-Carriage documentation is here: https://github.com/Armchair-Heavy-Industries/Xol-Toolhead/blob/main/docs/xol_carriage_assembly.md<br/>
> * A4T uses standard length probe modules for Xol-Carriage (even with UHF hotends in A4T).<br/>
> * Monolith Gantry users should go with the Monolith specific Xol-Carriage mod: [Monolith_Xol-Carriage](https://github.com/Armchair-Heavy-Industries/Armchair-Usermods/tree/main/files/Xol-Toolhead/Monolith_Xol-Carriage)<br/>

<br/><br/>

> [!WARNING]
> ### Front Idlers  
> A4T can collide with the stock voron front idlers for Trident and 2.4 when the toolhead is in the front corners of the build area. This can cause issues with the homing sequence when homing X if the toolhead is at the front of the gantry on Y. <br/><br/>
> Fully compatible idlers:<br/>
> * clee's [BFI (Beefy Front Idlers)](https://github.com/clee/VoronBFI)  <br/>
> * Ramalama2's [Front Idlers](https://github.com/Ramalama2/Voron-2-Mods/tree/main/Front_Idlers)  

<br/>

## Bill of Materials (BOM)
***`*Not including carriage hardware`***
| Qty | Item                                          | Notes                        |
| --- | --------------------------------------------- | ----------------------------------------------------------------------------------------- |
| 4   | M3 Square Nut (DIN 562)                       | Yes, square nuts. They don't spin in a slot like hex nuts                                  |
| 3   | M3 x 8 SHCS                                   | 2x Top cowling mounting. 1x Toolhead board mount to back of Xol Carriage                  |
| 2   | M3 x 6 BHCS or Waferhead screw                | Either of these screw types work. The important part is 6mm thread <br/> `This is only for Xol Carriage. If you use Tap or other Voron carriage, you already have longer SHCS where the hotend adapter slots under` <img src='docs/images/xol_carriage_screws.png' width=320 alt="tap screws" align='right'> | 
| 2   | M3 x 50 SHCS                                  | Bottom cowling mounting screws. The same as are in the bottom of Stealthburner            |
| 2   | * M3 x 16 SHCS or BHCS (WWBMG)<br/><br/>* M3 x 12 SHCS or BHCS (Sherpa-Mini)<br/><br/>* 1xM3 x 20 + 1xM3 x 16 SHCS or BHCS (WWG2)                         | Attach extruder to cowling                 |
| 2   | 4010 Blower Fan                               | Recommended blower: GDStime 12,000 RPM 24v. (<a href="https://www.aliexpress.com/item/1005005094153190.html">Ali Express</a>) <br/><br/>`⚠️ BERSERKER VINDR 4010 and HoneyBadger 9K 4010 fans known to be incompatible`                                                       |
| 1   | 2510 Axial Fan                                | Recommended fan: Delta Electronics 15,000 RPM 5v ASB02505SHA-AY6B (<a href="https://www.digikey.com/en/products/detail/delta-electronics/ASB02505SHA-AY6B/7491489">DigiKey</a>) <br/><br/> `⚠️ GDStime 2510 fans have been measuring as ~10.4mm thick. A workaround is to "sink" the hotend fand duct 0.4mm into the print bed with the slicer before printing.`|
| 3   | Neopixel LED PCB                              | The same kind as used in Stealthburner. Get the solder pad version. <br/> `Wiring diagram (click to enlarge) ---->`  <img src='docs/images/LED_wiring_order.jpg' width=60 alt="LEDs" align='right'>  <br/>`Different length wires for different Cowling types`                    |
| 9   | Lengths of 28 AWG or 26 AWG wire              | To make the LED harness      |
| 1   | Connector and required crimps                 | To make the LED harness      |
| 1   | Hotend                                        | Recommended hotend:<br/>*  **Dragon HF** with **Triangle Lab ZS-MZE-HF** (<a href="https://trianglelab.net/products/zs%C2%AE-mze%E2%84%A2-melt-zone-extender?VariantsId=11381">trianglelab.net</a>)<img src='docs/images/DragonHF+MZE.png' width=120 alt="Dragon" align='right'> <br/> Alternatives: <br/>* Dragon UHF or UHF-Mini <br/>* Dragon Ace `use the included 3mm spacer`<br/>* Dragon Ace with MZE `use the included 3mm spacer`<br/>* Rapido HF or UHF<br/>* NF-Crazy Volcano `May melt plastic behind status LED without tape insulation` <br/>* Revo-Voron<br/>* Bambulab<br/>* TZ-V6-2.0 <br/><br/>`volcano blocks with oversize heater cartridges may require some insulation tape (aluminium/reflective) on the back of the LED housing that faces the hotend.`      |
| 4   | Hotend screws                                 | Should come with your hotend. Dragon/Rapido usually use M2.5 x 8mm SHCS                   |
| 1   | Extruder                                      | Recommended Extruder:<br/>* Modified WW-BMG with Bondtech RIDGA v2. ([3mf files here](3mf/WW-BMG%20for%20A4T/))<br/> Alternatives: <br/>*Sherpa-Mini  <br/>*VZ-Hextrudort-Low <br/>*LGX-Lite <br/>*E3D Roto Vitamins <br/>*Wrist-Watch G2 <br/>*Orbiter 2.0 <br/> <br/>`⚠️ Sherpa-Mini not supported with UHF hotends`   |
| 2   | M3 threaded heat insert                       | Standard Voron spec: M3 x 5 x 4                                                           |
| 2   | 20mm or 21mm 3mm internal threaded stand off  | To attach toolhead board to the back of the extruder motor and third mounting point on the back of Xol Carriage. <br/>`Length will depend on the motor you use. It needs to line up the toolhead board holder with the back of the Xol Carriage.`                   |

## Printing parts
### Print settings
Parts are meant to be printed in 0.2mm layer heights, 0.25mm first layer should be OK. Other layer heights will cause the built-in supports to fail or fuse to the printed part.<br/>
Print settings will depend on your printer setup / filament used / phase of the moon/etc.<br/>
The parts are not pre-scaled for any particular filament type. You will need to tune the filament you use for correct shrinkage compensation to get good results. Development was done with multiple brands of ASA and ASA-CF filaments (each individually tuned).<br/>

General voron-like settings are a good starting point for 0.4mm wall widths (four walls, 5 top/bottom layers and 40% infill).<br/>
The print setup was tested with 0.5mm nozzle printing 0.55mm line widths with 3 walls and 40% infill with good results.<br/>

You're printing a toolhead, not a trinket or a toy. You should be aiming for high strength with strong layer adhesion. I.e. print it slower/hotter if you have bad layer adhesion. It doesn't matter if it takes over 2 hours to print the main body.<br/>

> [!TIP] 
> ### Printed Parts Configurator<br/>
> A great way to understand which files to print is by using this amazing configurator from **Corunir**: <a href="https://a4t.wizards-enclave.net/">https://a4t.wizards-enclave.net/</a>

<br/><br/><br/><br/>

> [!WARNING]
> ### Blower fan fit  
> `If your blower fans are not a slight friction fit, you likely had shrinkage compensation or EM issues. You can probably get away with using some masking tape on top of a loose fan to save a reprint in a pinch.` <br/>
> <br/>
> Fans should go in with a slight friction fit. DO NOT FORCE THEM IN. Your print settings aren't right if the fans are too tight. More shrinkage compensation or less EM depending on if you're over extruding or not.


## Assembly
### LED Harness (optional)
(click to open full size image)<br/>
<img src='docs/images/LED_wiring_order.jpg' width=250 alt="LED Harness"><br/>
Skinny wire needed, read the BOM.

### Assembly Steps

| <center>Notes</center>                                                                                                | Images|
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----: |
| Remove the built-in supports from the printed parts|<img src='docs/images/remove_supports.png' width=250><br/><img src='docs/images/remove_supports2.png' width=250><br/><img src='docs/images/remove_supports3.png' width=130> |
| Attach the LED filter to the LED diffuser. <br/>`a drop of superglue is handy here`                                   | <img src='docs/images/filter_assembly.png' width=100> |
| Install the LED filter/diffuser assembly into the cowl <br/>`it should push into place and stay put`                  | <img src='docs/images/install_filter.png' width=150> |
| Put the Status LED into the LED carrier <br/>`the one closest to the connector`                                       | <img src='docs/images/LED1_in_carrier.png' width=150> |
| Install the LED harness into the Cowl                                                                                 |       |
| &nbsp; &nbsp; &nbsp;1. Thread the two nozzle LEDs through the holder part of the cowl from the top and out the bottom | <img src='docs/images/LEDs_into_cowl1.png' width=150><img src='docs/images/LEDs_into_cowl2.png' width=150> |
| &nbsp; &nbsp; &nbsp;2. Install the middle LED of the chain into it's slot <br/><br/> `If the LEDs are tight to insert, run a small flat head screwdriver along the edges of the LED slots to open them up a bit.`                                            | <img src='docs/images/LEDs_into_cowl3.png' width=150> |
| &nbsp; &nbsp; &nbsp;3. Put the last LED into the other slot                                                           | <img src='docs/images/LEDs_into_cowl4.png' width=150> |
| &nbsp; &nbsp; &nbsp;4. The wires between the 2nd and 3rd LED go back up over the top of the Status LED holder         | <img src='docs/images/LEDs_into_cowl5.png' width=150> |
| Put the 2510 HE fan in place. <br/>`It will need to be angled in, slightly top first. The wires should be exiting from the top` <br/><br/> `⚠️ Don't push on the hub of the fan 😢` <img src='docs/images/warn2510.png' width=80 align=top> | <img src='docs/images/2510_install1.png' width=150> |
| Lock the 2510 HE fan in place by sliding the HE fan duct up until the flexture locks.<br/>`⚠️ Careful, don't pinch any wires`| <img src='docs/images/2510_install2.png' width=150> |
| Tidy up the LED harness wires in the little hooks. `the left blower fan will lock them in soon`                       | <img src='docs/images/LED_wires1.png' width=150> |
| ***Install the 4010*** ~~inserts~~ ***backflow inhibitors***                                                                                        |       |
| &nbsp; &nbsp; &nbsp;1. take the front cover off the 4010 blower fan<br/>`This is easy on gdstime fans. Might not be possible on Delta fans`  | <img src='docs/images/4010_remove_front.png' width=150> |
| &nbsp; &nbsp; &nbsp;2. Use some superglue or acetone to glue the ~~insert~~ ***backflow inhibitor*** in place<br/>`Use the spacer to line it up properly`                 | <img src='docs/images/glue_4010_insert.png' width=150><img src='docs/images/4010_insert_top.png' width=70> |
| &nbsp; &nbsp; &nbsp;3. Put the front cover back on the fan                                                            | <img src='docs/images/4010_insert_cover.png' width=150> |
| &nbsp; &nbsp; &nbsp;4. Remove the little handle and sand/file the ~~insert~~ ***backflow inhibitor*** flush with the blower opening                | <img src='docs/images/4010_insert_flush.png' width=150> |
| Time to put the blower fans in `Slide them into each side with the opening at the bottom`  <br/><br/>`*Fans should go in with a slight friction fit. DO NOT FORCE THEM IN. Your print settings aren't right if the fans are too tight. More shrinkage compensation or less EM depending on if you're over extruding or not.`                           | <img src='docs/images/install_4010s.png' width=150> |
| Attach your hotend                                                                                                    | <img src='docs/images/install_hotend.png' width=150> |
| Put all the square nuts in their places for later                                                                     | <img src='docs/images/install_square_nuts.png' width=150> |
| &nbsp; &nbsp; &nbsp;* Two under the extruder mounting points                                                          | <img src='docs/images/install_square_nuts_ext.png' width=150> |
| &nbsp; &nbsp; &nbsp;* Two in the back behind the exturder `Xol-Carriage only`                                         | <img src='docs/images/install_square_nuts_xol-carriage.png' width=150> |
| ***Main cowl is ready, time for the extruder***                                                                       |       |
| Make sure you used long enough screws to hold your stepper motor to the extruder and install the 20mm standoffs behind the motor                         | <img src='docs/images/Extruder_standoffs.png' width=150> |
| Attach the toolhead board mount and toolhead board to the standoffs `THB mounts, except for Sherpa-Mini, need 2x M3 heatsets installed before this step` | <img src='docs/images/Extruder_standoffs_thb.png' width=150> <img src='docs/images/Extruder_standoffs_thb_pcb.png' width=150>  |
| Put the Extruder Adapter in place on top of the cowl<br/>`*Not used with Sherpa-Mini or on UHF hotend cowls` <br/><br/>`⚠️ Don't forget the PTFE tube between extruder and hotend`        | <img src='docs/images/extruder_adapter.png' width=150> |
| :information_source: **Clockwork2 carriage/Tap users**: Don't forget the 2x M3x8 SHCS that go behind the adapter      | <img src='docs/images/extruder_adapter_cw2.png' width=150> |
| Attach the extruder to the main cowl <br/><br/>`⚠️ If using G2/Orbiter cowl for CW2/Tap carriage, the right screw for the extruder has to wait until the end.`  | <img src='docs/images/attach_extruder.png' width=150> |
| Time to wire it all up                                                                                                | <img src='docs/images/wired_up.png' width=150> |
| &nbsp; &nbsp; &nbsp;Make sure to keep wires out of the carriage screw keep clear zone                                 | <img src='docs/images/wire_keep_out_area.png' width=150> |
| &nbsp; &nbsp; &nbsp;Use the cable tie slots to keep everything tidy                                                   | <img src='docs/images/cable_tie_slots.png' width=150> |
| ***Finally, we can put this thing on the printer!***                                                                   |       |
| Ensure the screws already in the carriage have more than 3mm of exposed thread to hook the toolhead on to. <br/>`If they don't, the toolhead won't be able to slot into place`                | <img src='docs/images/carriage_screws.png' width=150> |
| Put the third toolhead board mounting screw into the back of Xol carriage, leaving 4 to 5mm of exposed threads        | <img src='docs/images/thb_third_screw.png' width=150> |
| Hook the toolhead board mount over third mounting screw and slide the completed toolhead down onto the screws that are pre-placed in the carriage.                                 | <img src='docs/images/hanging_toolhead_screws.png' width=150> |
| Tighten up all the screws:<br/>* 2x M3x50 bottom screws<br/>* 2x screws that were already in the carriage `access via the driver holes`<br/>* 2x M3x8 top screws<br/>&nbsp; &nbsp; &nbsp;** From the front for CW2/Tap<br/>&nbsp; &nbsp; &nbsp;** From the back for Xol Carriage<br/>* 1x M3x8 under the toolhead board (Xol Carriage only)                            |  <img src='docs/images/final_screws_front.png' width=150>  <img src='docs/images/final_screws_back.png' width=150>       |
| Remember to hook up your probe wires from the carriage to the toolhead board, if you're using one. <br/>`and your endstop wires if you haven't figured out sensorless yet`         |       |
| Make sure you double check your software setup `especially endstop location`                                          |       |

<br>

### The Results
After six months of development, CAD, CFD, trial and lots of error. Finally, A4T has better IS results, better cooling results and a new look compared to what I have been doing the last few years.

This is a comparison of part cooling between Xol and A4T. 
These prints were completed on the same printer, with the same gcode, same filament, the same hotend and part cooling fans (~~inserts~~ ***backflow inhibitors*** installed for A4T test).
![Comparison](docs/images/shuriken.png)

![CFG](docs/images/cfd.png)

### Credits
* Huge thanks for the support from the AHI team.
* Also to the Crew/Contributors at Voron Design
* Big shoutout to [yellowfish543](https://github.com/yellowfish543/StdToolheadOpenfoam/) for the CFD insights that unlocked the potential of this design.
* weaslus for insisting that the 4010 inserts get renamed to "backflow inhibitors"
* Corunir for the configurator wizard

> [!TIP] 
> ### You can help support the development of Armchair Projects.<br/>
> Donate at https://ko-fi.com/armchair<br/>
[![ko-fi](docs/images/Ko-fi_TextLogo.png)](https://ko-fi.com/armchair)

## Enjoy using A4T
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

### License clarification regarding non-commercial use:
The non-commercial aspect of this license is for cases where A4T is the product, not the use of A4T to create products.<br/>
I.e. If you wish to sell A4T as a product, you would need to seek a commercial license before doing so. </br>
It is NOT intended to prevent the use of A4T in a printer that you use to provide commercial services. If you want to run A4T as a toolhead for your print farm printers, go right ahead.
