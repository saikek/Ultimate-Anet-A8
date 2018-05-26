# TODO
* Не работает экран никакой
* Непонятно что с кулерами

* Замена микрошага Z на 1/32 пинами
* Проверить работает ли нагреватель E0
* Проверить работает ли датчик E0
* Проверить работает ли датчик Hotbed
* Нагреватель Hotbed
* Настроить вентиляторы с ОС через адаптер
* SD CARD support

# Done

* Пищит драйвер 8825 -> понизил ток с 8.5 до 7.5
* Extruder direction -> changed code to `#define INVERT_E0_DIR true`
* Endstop Not working -> Had to physically move Black top pin in the middle on each endstop.
* Z-Endstop sensor test -> OK, works (same re-pin was required as for end) 

* Fan (Extruder) -> had to re-pin & connect to 12/24v pin. Will think about using adapter from aux.
* Fan (Part cooling) -> re-pin & connected to FAN

* Hotbed TH -> had to remove pins & insert into 2-socket slots.
* Hotbed E1 -> had to remove pins & insert into 2-socket slots.