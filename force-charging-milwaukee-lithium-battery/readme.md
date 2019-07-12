# Don't do this at home

## Don't do this unless you have an extremely firm grasp of both lithium-battery and DC-power engineering

### Don't do this at all.

![](18v-milwaukee-lithium-via-nicad-charger.jpg)

## Why you don't want to do this:

Lithium cells have kind of a ... reputation.  They're kinda known for exploding.  Now, 18650 cells are generally quite a bit more safe than headline-capturing lithium batteries like lithium-polymer ones, but they still can be bad news if mistreated.

One isolated 18650 cell is actually pretty safe, but when you start connecting them in a high-ish voltage circuit, you start needing to hire some dedicated electronics to make sure they're treated well.  A "BMS" battery management/balancing board handles this task in most applications, communicating with each individual element of the wired series, as depicted here:

![](using-discharge-poles-to-circumvent-bms.png)

Modern power-tool companies out of a combination of...

* wanting to maximize profits by minimizing competing replacements/hardware
* knowing shadetree hardware will likely do an inferior job of battery-TLC

...have made communicating with the BMS board a pain in the ass. Instead of 2 poles for + and -, there's now a bunch of pins on power-tool lithium packs. Some pins for comms, some for charging, some for discharging, etc.  But note in the diagram above, the battery series still has +/- poles available: the discharge pins.

The reason you don't want to charge your lithium cell pack using the discharge pins (besides the obvious) is because you're circumventing the circuitry that protects the cells -- and you -- from potentially exploding.