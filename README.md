# Galileo 2

## NOTE: Galileo 2 is "Public Beta" in its current state.  CAD will be released once initial feedback has been considered.

![Image](./images/g2extruders.png)

## Welcome everyone, to Galileo 2!

Here you will find all of the files for the Galileo 2 projects, including a Voron Stealthburner drop-in Extruder (G2E), Z-Drives (G2Z) for V2-style printers (including V2, Micron, etc.), and a Standalone Extruder (G2SA) with mounting options for Orbiter-2.0-style or Sherpa-Mini-style mounts.

### <ins>TO NOTE!  ONLY the kits sold by LDO are "official" Galileo 2 kits!</ins>

For those that are curious about what Galileo 2 offers over Galileo 1, here's a short list of benefits:
 * Galileo 2 is a full redesign, moving to a 9:1 gear ratio and optimizing the gearbox design over Galileo 1.  No parts from Galileo 1 are reused with Galileo 2.
 * Custom 9T stepper with a taller spur gear resulting in 20% higher contact surface area than existing 10T stepper designs, resulting in better wear characteristics and power transfer.
 * Proper meshing of gears due to number of stepper teeth being divisible by number of planets (9T sun / 3 planets), which gives even loading on the planets / sun gear and improves wear characteristics and power transfer.  Previous designs with 10T steppers had uneven loading on the planet gears.

## Klipper Settings for G2 Extruders (G2E and G2SA)

You must update both the gear_ratio and rotation_distance in your Klipper configuration and do a standard
[extruder calibration](https://docs.vorondesign.com/build/startup/#extruder-calibration-e-steps) after installing the Galileo 2 Extruder. Additionally, your run_current will need to be updated.
```ini
[extruder]
rotation_distance: 47.088
gear_ratio: 9:1
microsteps: 16

[tmc2209 extruder]
run_current: 0.6
```

## Klipper Settings for G2 Z Drivers (G2Z)

You must update both the gear_ratio and rotation_distance in your Klipper configuration after installing the Galileo 2 Z Driver. Additionally, your run_current will need to be updated.
```ini
[stepper_z]
rotation_distance: 40
gear_ratio: 9:1
microsteps: 32

[tmc2209 stepper_z]
run_current: 0.8
```

<p align="center">
  <img width="320" height="214" src="./images/g2gears.gif" />
</p>
