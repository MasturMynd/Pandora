# Pandora

Have you ever been trying to add a mod to your V0 but quickly realize that it won't fit due to travel restrictions? Have you wanted to transition to a front mounted x rail but didn't want to lose Y travel? If you've said yes to either, allow me to present Pandora, a gantry mod for the Voron V0 that allows 142mm of X travel and 127mm of Y travel within the stock frame.

![Image of Pandora Gantry](./Images/Pandora_Complete_Gantry.png)

The Goal
---
I've been wanting to be able to incorporate a nozzle brush, purge bucket, sexbolt mod, etc., but there just wasn't enough travel with the stock gantry. The added travel outside the bounds of the bed should allow for a plethora of additional mods as well as a higher density of mods within the stock frame.

What's the Catch?
---
In order to use this mod you will need a new linear rail for X motion. In order to achieve 144mm of X travel, the stock 150mm rail won't cut it. The bearing block would fall off the rail before you hit full travel. On top of that, you'll also need some 3x14mm pins and a few extra F623 bearings. Aside from new parts you'll also have to account for the gantry being raised by ~8mm over stock. This means that the linear rails for Z motion may need to be raised and there's a possibility that things will get cramped under the tophat.

In addition, the stock side panel mounting will no longer work since the carriage for the Y rails protrudes over the extrusions. I highly recommend [Zero Panels](https://github.com/zruncho3d/ZeroPanels) as these add the extra room between the acrylic panels and the carriages with the added benefit of making panels easier to remove for cleaning and future upgrades.

The biggest hurdle for some is going to be that this setup currently requires sensorless homing. I am actively working to incorporate endstops into the design, but I refuse to sacrifice the additional travel that I've worked so hard to achieve.

BOM
---
| Part | Pandora | Stock | Diff | Sourcing |
| --- | --- | --- | --- | --- |
| **Front Idlers** | | | | | |
| 3x14mm Pin | 2 | 0 | 2 | [Amazon](https://www.amazon.com/uxcell-Stainless-Cylindrical-Support-Elements/dp/B07Y58JKMC/ref=sr_1_3?crid=12XNCA9O5NWIN&keywords=3x14mm%2Bpin&qid=1674715484&s=industrial&sprefix=3x14mm%2Bpin%2Cindustrial%2C93&sr=1-3&th=1) |
| M3x8 BHCS | 2 | 2 | 0 | |
| M3x10 BHCS | 2 | 2 | 0 | |
| M3x40 BHCS | 2 | 0 | 2 | |
| M3 Washer | 8 | 4 | 4 | |
| M3 Hex Nut | 2 | 2 | 0 | |
| F623-RS | 8 | 4 | 4 | |
| | | | | |
| **XY Joints** | | | | | |
| M2x6 FHCS | 8 | 8 | 0 | |
| 3x14mm Pin | 2 | 0 | 2 | [Amazon](https://www.amazon.com/uxcell-Stainless-Cylindrical-Support-Elements/dp/B07Y58JKMC/ref=sr_1_3?crid=12XNCA9O5NWIN&keywords=3x14mm%2Bpin&qid=1674715484&s=industrial&sprefix=3x14mm%2Bpin%2Cindustrial%2C93&sr=1-3&th=1) |
| M3x8 BHCS | 4 | 0 | 4 | |
| M3x10 BHCS | 2 | 0 | 2 | |
| M3x20 BHCS | 4 | 0 | 4 | |
| M3 Washer | 8 | 16 | 0 | |
| M3 Hex Nut | 6 | 6 | 0 | |
| M3 Threaded Insert | 2 | 4 | 2 | |
| F623-RS | 8 | 8 | 0 | |
| | | | | |
| **Drive Frames** | | | | | |
| M3x8 BHCS | 10 | 0 | 10 | |
| M3x10 BHCS | 2 | 2 | 0 | |
| M3x12 BHCS | 2 | 0 | 2 | |
| M3x25 BHCS | 4 | 0 | 4 | |
| M3x30 BHCS | 8 | 4 | 4 | |
| M3x35 BHCS | 4 | 20 | 0 | |
| M3x40 BHCS | 2 | 0 | 2 | |
| M3 Washer | 16 | 12 | 4 | |
| M3 Hex Nut | 10 | 10 | 0 | |
| M3 Threaded Insert | 10 | 8 | 10 | |
| F623-RS | 16 | 12 | 4 | |
| | | | | |
| **X Carriage** | | | | |
| MGN9-(H or C) Linear Guide Rail 180-200mm | 1 | 0 | 1 |[DFH](https://deepfriedhero.in/products/mgn9h-linear-rail?variant=40905213313193), [Amazon](https://www.amazon.com/gp/product/B07ZJMWGKH/,) |
| M3x8 BHCS | 4 | 0 | 4 | |
| M3x40 BHCS | 2 | 0 | 2 | |
| M3 Threaded Insert | 3 | 3 | 3 | |

After Installation
---
The first thing that you will want to do is head over to the Voron Design website to read about setting up sensorless homing. There's a fantastic article by none other than [clee](https://github.com/clee), [Setting Up and Calibrating Sensorless Homing](https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html).

Last, you'll want to ensure that your `printer.cfg` has been set up to take advantage of the extra room you've just unlocked without risking some sick high flying, mid air prints. You'll want to alter the `[stepper_x]` and `[stepper_y]` sections with the following machine limits:

```
[stepper_x]
...
position_endstop: 131
position_max: 131
position_min: -11
...

[stepper_y]
...
position_endstop: 125
position_max: 125
position_min: -2
...
```

Issues?
---
If you run into any trouble or have questions during assembly don't hesitate to ping me in the Voron Discord server (@Mastur_Mynd). Also, If you find any other sources for the above parts at comparative prices / quality (or better) please let me know!
