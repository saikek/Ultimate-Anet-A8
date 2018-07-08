# Hardware info
* Motors: Model: 42shdc3025-24b, LOT NO: 170802

* Step Angle: 1.8
* Microstepping: *
* Rated voltage:3.96V
* Rate Speed 1000 rmp
* Rated Current: 0.9A

# Vref Values (For Anet Motor):
| Driver  | Mode | Vref Value | JUMPER 1 | JUMPER 2 | JUMPER 3 |
| ------- | ---- | ---------- | -------- | -------- | -------- |
| DRV8825 |      | 0.45       |          |          |          |
| TMC2208 | 1/16 |            | TRUE     | TRUE     | FALSE    |
| TMC2130 | 1/16 |            | FALSE    | FALSE    | FALSE    |


# Vref Configuration:
X 0.8 (2208)
Y 0.8 (2208)
Z1 0.5 (2208)
Z2 0.50 (2208)
E 0.55 (drv8825)

see: https://learn.watterott.com/silentstepstick/faq/

# Calibrating useful commands:
 ```
G28 - Home all axis
G29 - Auto-level
M851 Z-1.1 - set offset for Z nozzle to -1.1
G1 Z0; Move nozzle to what it thinks is the zero height.
```

# DEFAULT_AXIS_STEPS_PER_UNIT
Somehow `DEFAULT_AXIS_STEPS_PER_UNIT` is not set when changing firmware, so I need to run manually command:

`M92 Z400` - which sets axis steps. If your model is too shrinked or pressed - it's because of this wrong value.

* 400 - Default Value & TMC2208 with microstepping x16
* 1600 - CRAZY NOISE

# Fast way to calibrate & test:
After you've done Auto-level this would help calibrate Z offset without homing X and Y. Saves lots of time, since you can run this code snippet 5 times in a row.

```
M851 Z-2.5;
M500;
G28 Z;
G1 Z0;
```

Previous calibrations:
* M851 Z-3.5; //100
* M851 Z-2.5; //400
* M851 Z-1.2; //1600
* M851 Z-0.6; //800 - NOK, in space



# Recovery & Flashing
[Good instruction on flashing][good-instruction]
[Fixing bricked][fixing-bricked]

# Issues during flashing:
```
avrdude: ser_open(): can't open device "\\.\COM5": The system cannot find the file specified.
```
Change port in configuration.

# See Shopping.md for prices and recommended items.
# See Upgrade.md for Upgrade recommendations

[good-instruction]: http://3dtoday.ru/blogs/407s/marlin-firmware-116-for-anet-a6/
[fixing-bricked]: http://www.instructables.com/id/HOW-TO-FIX-ANET-BRICKED-BOARD-USING-AN-ARDUINO-UNO/