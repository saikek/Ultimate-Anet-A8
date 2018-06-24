# Hardware info
* Motors: Model: 42shdc3025-24b, LOT NO: 170802

* Step Angle: 1.8
* Microstepping: *
* Rated voltage:3.96V
* Rate Speed 1000 rmp
* Rated Current: 0.9A

# Calibrating useful commands:
 ```
G28 - Home all axis
G29 - Auto-level
M851 Z-1.1 - set offset for Z nozzle to -1.1
G1 Z0; Move nozzle to what it thinks is the zero height.
```

# Fast way to calibrate & test:
After you've done Auto-level this would help calibrate Z offset without homing X and Y. Saves lots of time, since you can run this code snippet 5 times in a row.

```
M851 Z-2.5;
M500;
G28 Z;
G1 Z0;
```

# Recovery & Flashing
Good instruction on flashing 
http://3dtoday.ru/blogs/407s/marlin-firmware-116-for-anet-a6/

See nice instruction here:
http://www.instructables.com/id/HOW-TO-FIX-ANET-BRICKED-BOARD-USING-AN-ARDUINO-UNO/

# Issues during flashing:
```
avrdude: ser_open(): can't open device "\\.\COM5": The system cannot find the file specified.
```
Change port in configuration.

# See Shopping.md for prices and recommended items.
# See Upgrade.md for Upgrade recommendations 