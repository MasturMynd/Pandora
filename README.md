# Pandora

After weeks of planning, trial and error, CAD work and scrapping dozens of attempts, I present Pandora, a gantry mod for the Voron V0 that allows 144mm of X travel and 127mm of Y travel within the stock frame.

![Image of Pandora Gantry](./Images/Pandora_Complete_Gantry.png)

The Goal
---
I've been wanting to be able to incorporate a nozzle brush, purge bucket, sexbolt mod, etc., but there just wasn't enough travel with the stock gantry. The added travel outside the bounds of the bed should allow for a plethora of additional mods as well as a higher density of mods within the stock frame.

Something's Missing
---
The astute among you may have noticed that there are no tensioners or tensioner knobs for the motor mounts. That's because this design uses the stock designs for those items. Please hop over to the [Voron-0](https://github.com/VoronDesign/Voron-0) repo to pick these up if you don't already have them.

It wasn't all fun and games
---
This project was almost shelved several times in the short while that I've been working on it. There's a lot of little things that had to line up just right in order for something like this to be possible. I'm still not sure if it was a miracle, my ingenuity or complete and utter dumb luck that the stars aligned to make this happen.

What's the Catch?
---
In order to use this mod you will need a new linear rail for X motion. In order to achieve 144mm of X travel, the stock 150mm rail won't cut it. The bearing block would fall off the rail before you hit full travel. On top of that, you'll also need some 3x14mm pins and a couple of extra F623 bearings. Aside from new parts you'll also have to account for the gantry being raised by ~8mm over stock. This means that the linear rails for Z motion will need to be raised and there's a possibility that things will get cramped under the tophat.

The biggest hurdle for some is going to be that this setup currently requires sensorless homing as there isn't really a good place to put X or Y endstops.

BOM
---
| QTY | Part | Sourcing |
| --- | --- | --- |
| 1 | MGN7-H Linear Guide Rail 180-200mm | (unsourced) |
| or | MGN9-C Linear Guide Rail 180-200mm | [Amazon](https://www.amazon.com/ReliaBot-Linear-Carriage-Printer-Machine/dp/B094CYMC3S/ref=sr_1_5?crid=MVNUARB2CP82&keywords=MGN9c&qid=1661545206&s=industrial&sprefix=mgn9c%2Cindustrial%2C90&sr=1-5) |
| or | MGN9-H Linear Guide Rail 180-200mm | [DFH](https://deepfriedhero.in/products/mgn9h-linear-rail?variant=40905213313193), [Amazon](https://www.amazon.com/gp/product/B07ZJMWGKH/,) |
| 2 | 3x14mm Dowel Pins | [Amazon](https://www.amazon.com/Stainless-Support-Elements-Location-Yesallwas/dp/B0819FZM8F/) |
| 4 | F623 Bearings (V0 BOM Bearings) | [DFH](https://deepfriedhero.in/products/f623-rs-bearings?variant=40963862626473) |
| | The rest of the parts should be BOM leftovers | |

Issues?
---
If you run into any trouble or have questions during assembly don't hesitate to ping me in the Voron Discord server (@Mastur_Mynd). Also, If you find any other sources for the above parts at comparative prices / quality (or better) please let me know!
