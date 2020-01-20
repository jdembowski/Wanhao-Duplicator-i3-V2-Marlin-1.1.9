# Wanhao-Duplicator-i3-V2-Marlin-1.1.9

This has support for a Z stop induction sensor on the stock Melzi board that comes with the Wanhao Duplicator V2.1 (Monoprice Maker Select V2). 

The LCD will be corrupted unless you edit the Marlin file `ultralcd_st7920_u8glib_rrd.h` and locate the line that reads

```
//set optimization so ARDUINO optimizes this file
#pragma GCC optimize (3)
```

and change it to read

```
//set optimization so ARDUINO optimizes this file
//#pragma GCC optimize (3)
```

And the display should work after the firmware is built and pushed to the 3D printer.
