# BIGTREETECH-SKR-MINI-E3-V3-BLTouch-A-ZHoming
_Prerequisite: Knowledge of building your own Marlin firmware._

## My setup:
-	Ender 3 with stock screen
-	BIGTREETECH SKR Mini E3 V3
-	BLTouch clone with 3 wires plugged into Z-Probe, and 2 wires plugged into Z-Stop.
-	Ensure jumpers for Neo-PWR1 pins enable on board 5V PSU. Refer to page 6 of the [user manual](https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/blob/master/hardware/BTT%20SKR%20MINI%20E3%20V3.0/Hardware/BTT%20SKR%20MINI%20E3%20V3.0%20user%20manual.pdf).
-	Marlin version [2.1.2.1](https://github.com/MarlinFirmware/Marlin/releases/tag/2.1.2.1), built off the Creality Ender 3 with BTT SKR Mini E3 V3 [example configuration file]().
-	Ensure jumpers for Neo-PWR1 pins enable on board 5V PSU. Refer to page 6 of the [user manual](https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/blob/master/hardware/BTT%20SKR%20MINI%20E3%20V3.0/Hardware/BTT%20SKR%20MINI%20E3%20V3.0%20user%20manual.pdf).
  
### Configuration.h changes
```
#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
#define BLTOUCH
#define NOZZLE_TO_PROBE_OFFSET { 38, -5, -2 } // Use your own values
//#define MIN_SOFTWARE_ENDSTOP_Z 
#define AUTO_BED_LEVELING_BILINEAR
//#define MESH_BED_LEVELING
#define Z_SAFE_HOMING
```

### Configuration_adv.h changes
Make sure the below are commented (disabled)
```
//#define BLTOUCH_FORCE_SW_MODE
//#define BLTOUCH_SET_5V_MODE
//#define BLTOUCH_HS_MODE true
```
</br>

If you’re running the same setup as me, you can download the Configuration.h and Configuration_adv.h files with the above settings to build and test before making further changes.  
