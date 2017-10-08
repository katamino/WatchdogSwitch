# WatchdogSwitch

Power switch with watchdog timer

The IC with the built-in countdown timer monitors GPIO of MCU,
and the software on MCU sends pulse signals to GPIO at a fixed interval to re-set the timer in the IC.

The countdown timer on the watchdog does not reset when no pulse signals are sent due to an error on MCU.
The IC on the board will then stop providing the power to MCU and re-start providing the power to re-start the MCU

```
/WatchdogSwitch
  |-- /ATTiny
  |     |-- WDtimer.c    .c source file 
  |     |-- WDtimer.h    .h source file
  |
  |-- /Hardware
  |     |-- watchswitch_schematic_rev1.pdf     Circuit diagram
  
```
