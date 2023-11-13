# Galileo 2

## NOTE: Galileo 2 is "Public Beta" in its current state.  CAD will be released once initial feedback has been considered.

![Image](./images/g2extruders.png)

## Welcome everyone, to Galileo 2!

Here you will find all of the files for the Galileo 2 projects, including a Voron Stealthburner drop-in Extruder (G2E), Z-Drives (G2Z) for V2-style printers (including V2, Micron, etc.), and a Standalone Extruder (G2SA) with mounting options for Orbiter-2.0-style or Sherpa-Mini-style mounts.

For those that are curious about what Galileo 2 offers over Galileo 1, here's a short list of benefits:
 * Galileo 2 is a full redesign, moving to a 9:1 gear ratio and optimizing the gearbox design over Galileo 1.  No parts from Galileo 1 are reused with Galileo 2.
 * Custom 9T stepper with a taller spur gear resulting in 20% higher contact surface area than existing 10T stepper designs, resulting in better wear characteristics and power transfer.
 * Proper meshing of gears due to number of stepper teeth being divisible by number of planets (9T sun / 3 planets), which gives even loading on the planets / sun gear and improves wear characteristics and power transfer.  Previous designs with 10T steppers had uneven loading on the planet gears.

## Galileo 2 Resellers List
### <ins>TO NOTE!  ONLY the kits sold by LDO are "official" Galileo 2 kits!</ins>

| Reseller        | Location      | Website                                                                                                                         |
|---------------- |-------------  |-------------------------------------------------------------------------------------------------------------------------------  |
|    Fabreeko     |     USA       | https://www.fabreeko.com/                                                                                                       |
|     West3D      |     USA       | https://west3d.com/products/galileo-2-kit-by-jaredc01-ldo-motors-g2e-and-g2z-extruder-and-z-drive-kits?variant=43937791639764   |
|   Filastruder   |     USA       | https://www.filastruder.com/search?type=product&q=GALILEO2                                                                      |
|       DFH       |     USA       | https://dfh.fm/                                                                                                                 |
|      KB-3D      |     USA       | https://kb-3d.com/store/voron/989-ldo-motors-galileo-2-extruder-g2e-for-voron-1694715593330.html                                |
|    Sparta3d     |    Canada     | https://sparta3d.ca/products/galileo-2-extruder-g2-extruder-g2e?_pos=3&_sid=9e9c00f0f&_ss=r                                     |
|    3dlabtech    |    Canada     | www.3dlabtech.ca                                                                                                                |
|      Dremc      |  Australia    | www.dremc.com.au                                                                                                                |
|    PhaserFPV    |  Asutralia    | https://www.phaserfpv.com.au/products/ldo-galileo-2-kit?variant=42952037400747                                                  |
|  Uniqueprints   |  Australia    | https://uniqueprints.shop/?s=Galileo&post_type=product&type_aws=true                                                            |
|    OneTwo3d     |      UK       | https://www.onetwo3d.co.uk/product/ldo-galileo-2-extruder-kit/                                                                  |
|       3DO       |   Denmark     | https://3do.eu/accessory/1232-galileo-2-extruder-kit-by-ldo.html                                                                |
|     3Dparts     |   Austria     | https://www.3dparts.at/                                                                                                         |
|     Lecktor     |   Estonia     | https://lecktor.com/en/extruders/1480-galileo2-extruder-kit-g2e.html                                                            |
|      Zen3d      |   Hungary     | https://shop.zen3d.hu/ldo-galileo-2-extruder-g2e                                                                                |
|     Lab4450     |   Portugal    | https://lab4450.com/product/galileo-2-extruder-kit/                                                                             |
|  Levendig dsgn  | Netherlands   | https://shop.levendigdsgn.com/                                                                                                  |
|     Kris3d      |   Germany     | https://www.kris3d.de/                                                                                                          |
| Jacks Filament  |   Germany     | https://www.jacksfilament.com/Galileo-2-Extruder-Kit-G2E-by-LDO                                                                 |
|   partner-3d    |   Germany     | https://partner-3d.de/3d-druck-ersatzteile/                                                                                     |
|    Alchemy3d    |   Germany     | https://alchemy3d.de/products/ldo-galileo-2-extruder-kit-pre-order?_pos=1&_sid=6989ccc18&_ss=r                                  |
|    replimat     |   Germany     | https://replimat.eu                                                                                                             |
|      SWBAC      |    Kuwait     |  https://swbac.com/product-category/3d-printing/ldo/                                                                            |
|     Sugoi3d     |    Japan      | www.sugoi3d.jp                                                                                                                  |

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
