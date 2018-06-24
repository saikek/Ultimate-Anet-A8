# TODO
* Screen not working
* Set up fan's using special adapter
* SD CARD support
* X layers shifts after 30 minutes of printing

# Done

* Low-pitch nois on 8825 -> decreased voltage 0.85 to 0.75
* Extruder direction -> changed code to `#define INVERT_E0_DIR true`
* Endstop Not working -> Had to physically move Black top pin in the middle on each endstop.
* Z-Endstop sensor test -> OK, works (same re-pin was required as for end) 

* Fan (Extruder) -> had to re-pin & connect to 12/24v pin. Will think about using adapter from aux.
* Fan (Part cooling) -> re-pin & connected to FAN

* Hotbed TH -> had to remove pins & insert into 2-socket slots.
* Hotbed E1 -> had to remove pins & insert into 2-socket slots.
* Замена микрошага Z на 1/32 пинами -> Не надо
* LOW pitch noise from Z motors - replaced microstepping by pins (for now) - only first is in. used 2130 motor. 

* Problems with Z axis -> Used DRV8825 with voltage 0.6, used also E1 extruder connection for Z2 motor.
* Z motors always overheated - checked their specs / voltage - it looks like they are 0.9 volts, so Vref on DRV8825 should be 0.45 V.