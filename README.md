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

see: https://learn.watterott.com/silentstepstick/faq/

# Calibrating useful commands:
 ```
G28 - Home all axis
G29 - Auto-level
M851 Z-1.1 - set offset for Z nozzle to -1.1
G1 Z0; Move nozzle to what it thinks is the zero height.
```

# Fast way to calibrate & test:
After you've done Auto-level this would help calibrate Z offset without homing X and Y. Saves lots of time, since you can run this code snippet 5 times in a row.


M851 Z-1.2; //1600
M851 Z-0.6; //800 - NOK, in space
//1600 - CRAZY NOISE

```
M851 Z-2.5;
M500;
G28 Z;
G1 Z0;
```

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