Conky temperature CPU (example)

sensors
```
mariusz@laptop-debian:~$ sensors
coretemp-isa-0000
Adapter: ISA adapter
Physical id 0:  +38.0°C  (high = +100.0°C, crit = +100.0°C)
Core 0:         +37.0°C  (high = +100.0°C, crit = +100.0°C)
Core 1:         +36.0°C  (high = +100.0°C, crit = +100.0°C)

acpitz-virtual-0
Adapter: Virtual device
temp1:        +37.0°C  (crit = +98.0°C)
temp2:        +35.0°C  (crit = +126.0°C)

pch_skylake-virtual-0
Adapter: Virtual device
temp1:        +35.5°C  

mariusz@laptop-debian:~$ 
```
hwmon
```
mariusz@laptop-debian:~$ ls /sys/class/hwmon
hwmon0  hwmon1  hwmon2
mariusz@laptop-debian:~$ 
```
hwmon name
```
mariusz@laptop-debian:~$ cat /sys/class/hwmon/hwmon0/name
acpitz
mariusz@laptop-debian:~$ cat /sys/class/hwmon/hwmon1/name
pch_skylake
mariusz@laptop-debian:~$ cat /sys/class/hwmon/hwmon2/name
coretemp
mariusz@laptop-debian:~$ 
```
conky
```
Temp cpu1$alignr ${hwmon 2 temp 2}°C
Temp cpu2$alignr ${hwmon 2 temp 3}°C
```
screenshot

<img src="https://skandyns.github.io/img/conky-cpu-temp.png"/>


