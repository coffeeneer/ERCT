
# Enraged Rabbit Cotton Tail

<p align="center">
  <img src="Assets/heroimage_ERCT.png" alt='ERCT' width='70%'>
</p>

<!-- TODO: hero image is still the V2 render; replace with a V3 render/photo -->

## Introduction

The Enraged Rabbit Cotton Tail (ERCT) buffer system is designed to attach directly to the ERCF V3. It is also designed to reduce as much resistance as possible in the filament path, creating a consistent system for calibration.

This system is also designed to reduce the buffer length, while the loops are defined by the amount of tube you use from the encoder to the tool head.
V3 is a redesign of the V2 buffer. The single-piece support arm of V2 has been replaced by a modular, stackable arm made of a hub plate and separate buffer walls, the buffer wheel is larger, and the electronics end cap now uses a universal electronics box.

**Features include:**

* Large central buffer wheel - now ~97mm in diameter (V2: ~88.5mm), reducing the bend radius of the filament even further. The wheel is a two-part design with a screw-in grip.
* Modular arms - each gate is built from an arm hub, buffer walls and secondary buffer walls, so parts are smaller and easier to print and replace.
* Inline connection - connects directly to the 2020 extrusion via the arm mount.
* Short Buffer Length - Can operate as short as 500mm in buffer length.
* Stackable Arm - Each arm is stackable for whatever combination of gates you want. Printed double-thread axles are provided for 4, 6, 8 and 9 gates.
* Crank - a printed crank to turn the buffer wheels when loading filament.
* Universal electronics box - the end cap carries a generic electronics box instead of the BTT MMB-specific case from V2.

***

## What changed from V2

| Area | V2 | V3 |
| --- | --- | --- |
| Support arm | One-piece `Support_Arm_xN` (~210 x 197mm) + `Support_Arm_Mount_xN` | Modular: `Arm_Hub_xN`, `[a]Arm_Mount_xN`, `[a]Bufferwall_inlet_xN`, `[a]Bufferwall_x2N`, `Secondary_buffer_wall_x2_xN` |
| Buffer wheel | One-piece, ~88.5mm diameter | Two-piece (`Buffer_Wheel_xN` + `Buffer_Wheel_screw-in-grip_xN`), ~97mm diameter |
| Axle | Double-thread axle, 4/5/6/8/9/10/12 gates, with axle spacers | Double-thread axle, 4/6/8/9 gates, ~10mm shorter for the same gate count. Axle spacers are no longer used |
| Knut | ~16mm tall | Redesigned, ~7mm tall |
| Crank | — | New |
| End cap | BTT MMB end cap or end cap without electronics box | `End_Cap_Hub_V3`, `End_Cap_Mount`, end cap buffer walls and secondary walls |
| Electronics box | BTT MMB-specific box + lid | `Universal_Box_Base_V3` + `Universal_Box_Lid_V3` (same 72.5 x 130mm footprint, taller lid) |
| Coupler block | `[c]_Coupler_Block_xN` + LED carrier/apron | Removed |
| LED soldering jig | Included | Not included |

The printable parts are in the `Rev2/` folder. The CAD assembly (`CAD/ERCT V3_Rev_2.step`) shows an 8-gate build.

***

## Acknowledgements

ERCT was designed to simplify the buffer design and integrate cleanly with ERCFv2. I thank the entire team from the ERCF V2 team, especially Moggie, for bringing me onto the team. I also have my home server, Fizzy's Tech, on Discord to thank for the countless support and hosting of the Beta development on that server. Jose from Fizzy's Tech was instrumental in this development as he was part of the system's early development and early testing. There are numerous testers who have helped as well, making suggestions throughout the beta cycle. I want to give a special shout-out to Wolffy01 and gsx8299 for their contributions to ideas, testing and mods.&#x20;

Questions related to this buffer can be directed at <https://discord.com/channels/460117602945990666/909743915475816458> or you may visit my home server at <https://discord.gg/Gs2vAtK7T7>

Terrance Lam
@kinematicdigit

***

## BOM

### Each arm group/channel:

* (1) 608 ZZ Bearing (same as ERCP - skateboard bearings will work as well)
* (2) 8mm M3 socket head screws (SHCS)
* (2) M3 threaded inserts (M3x5x4mm) Heat Sets
* (1) M3 Roll-in Spring T-nut (for attaching to 2020 extrusions)
* (1) ECAS
* PTFE Tubing (4mm OD/3MM ID Clear)

### End cap:

* (4) 8mm M3 button head screws (BHCS)
* (4) M3 threaded inserts (M3x5x4mm) Heat Sets

### Universal electronics box:

* (2) 8mm M3 button head screws (BHCS)
* (2) M3 threaded inserts (M3x5x4mm) Heat Sets
* Controller board *(V2 used a BTT MMB CAN board)*

<!-- TODO: list which boards fit the universal box -->

### Filament sensing (per arm):

* (1) Microswitch
* (1) 5.5 mm ball bearing
* (2) 8 or 10 mm M2 self-thread screws

***

**FULL BUILD INSTRUCTIONS FOUND IN THE ERCF V2 BUILD GUIDE**

**LOADING THE BUFFER**

There are several ways to load the buffer. Use this as a reference but you may find other ways to load that is easier for you. The photos below show the V2 buffer, but the procedure is the same.

<!-- TODO: the "divide by 230mm" figure was measured on the V2 wheel; the larger V3 wheel holds more filament per row, so this number needs re-measuring -->

| <img src="Assets/IMG_6671%20Small.png" /> | To load the buffer, filament from your reverse Bowden. Try your best to work with the natural curl of the filament and feed it till you see it pop out on top. |
| -: | :- |
| <img src="Assets/IMG_6674%20Small.png" /> | Grab it from up top, and curl it back into one of the multiple filament loading holes located along one side of the buffer wheel. |
| <img src="Assets/IMG_6675%20Small.png" /> | Turn the wheel until you have the number of rows needed for your tube length between the ERCF encoder and the tool head (to calculate the right length, measure the tube and divide by 230mm. This will equal the number of rows you need to wrap around the wheel - maximum of 7). |
| <img src="Assets/IMG_6676%20Small.png" /> | Back below, grab the filament on the wheel and pull it out. |
| <img src="Assets/IMG_6677%20Small.png" /> | Give yourself some length (about 30 cm). |
| <img src="Assets/IMG_6678%20Small.png" /> | Feed back into the tube located there. |
| <img src="Assets/IMG_6679%20Small.png" /> | It will feed through, and you should feel some resistance from the trap; press on the top hat to help it through. |
| <img src="Assets/IMG_6680%20Small.png" /> | The final step is to push the filament flush to the opening so it doesn’t catch on the selector. That’s it. Load it all up, and away you go! |

***

## Options & User Mods

* `Options/` - PTFE arm anchor and magnetic PTFE couplers (unchanged from the V2 180° build option).
* `User_Mods/` - community mods carried over from V2. These were designed for V2 and may not fit V3.
