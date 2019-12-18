# Ender-5-SKR-Mini-E3-v1.2
As requested I uploaded my Configuration.h and Configuration_adv.h files.

Things that are changed (From the config\examples\BigTreeTech\SKR Mini E3 1.2 folder) are listed below:

# Configuration.h

From:
//#define CUSTOM_STATUS_SCREEN_IMAGE

To:
#define CUSTOM_STATUS_SCREEN_IMAGE

From:
#define PREVENT_COLD_EXTRUSION
#define EXTRUDE_MINTEMP 170

To:
#define PREVENT_COLD_EXTRUSION
#define EXTRUDE_MINTEMP 180


From:
#define PREVENT_LENGTHY_EXTRUDE
#define EXTRUDE_MAXLENGTH 600

To:
#define PREVENT_LENGTHY_EXTRUDE
#define EXTRUDE_MAXLENGTH 800


From:
#define USE_XMIN_PLUG
#define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
//#define USE_XMAX_PLUG
//#define USE_YMAX_PLUG

To:
//#define USE_XMIN_PLUG
//#define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
#define USE_XMAX_PLUG
#define USE_YMAX_PLUG


From:
#define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 400, 93 }

To:
#define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 800, 93 }


From:
#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN

To:
//#define Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN


From:
#define NOZZLE_TO_PROBE_OFFSET { 10, 10, 0 }

To:
#define NOZZLE_TO_PROBE_OFFSET { -41, -12, 0 }


From:
#define INVERT_Z_DIR false

To:
#define INVERT_Z_DIR true

From:
#define X_HOME_DIR -1
#define Y_HOME_DIR -1

To:
#define X_HOME_DIR 1
#define Y_HOME_DIR 1

From:
#define X_BED_SIZE 235
#define Y_BED_SIZE 235

To:
#define X_BED_SIZE 220
#define Y_BED_SIZE 220


From:
#define Z_MAX_POS 250

To:
#define Z_MAX_POS 300

From:
#define MIN_SOFTWARE_ENDSTOP_Z

To:
//#define MIN_SOFTWARE_ENDSTOP_Z

From:
#define GRID_MAX_POINTS_X 3

To:
#define GRID_MAX_POINTS_X 5

From:
//#define MESH_EDIT_GFX_OVERLAY   // Display a graphics overlay while editing the mesh

To:
#define MESH_EDIT_GFX_OVERLAY   // Display a graphics overlay while editing the mesh

From:
#define GRID_MAX_POINTS_X 3
To:
#define GRID_MAX_POINTS_X 5

From:
//#define MESH_G28_REST_ORIGIN

To:
#define MESH_G28_REST_ORIGIN

From:
//#define MESH_EDIT_MENU

To:
#define MESH_EDIT_MENU


From:
#define LEVEL_BED_CORNERS

To:
//#define LEVEL_BED_CORNERS

From:
#define EEPROM_AUTO_INIT

To:
//#define EEPROM_AUTO_INIT

From:
// Preheat Constants
#define PREHEAT_1_LABEL       "PLA"
#define PREHEAT_1_TEMP_HOTEND 185
#define PREHEAT_1_TEMP_BED     45
#define PREHEAT_1_FAN_SPEED   255 // Value from 0 to 255

#define PREHEAT_2_LABEL       "ABS"
#define PREHEAT_2_TEMP_HOTEND 240
#define PREHEAT_2_TEMP_BED    110
#define PREHEAT_2_FAN_SPEED   255 // Value from 0 to 255

To:
// Preheat Constants
#define PREHEAT_1_LABEL       "PLA"
#define PREHEAT_1_TEMP_HOTEND 200
#define PREHEAT_1_TEMP_BED     60
#define PREHEAT_1_FAN_SPEED   255 // Value from 0 to 255

#define PREHEAT_2_LABEL       "ABS"
#define PREHEAT_2_TEMP_HOTEND 240
#define PREHEAT_2_TEMP_BED    100
#define PREHEAT_2_FAN_SPEED   255 // Value from 0 to 255

From:
#define NOZZLE_PARK_POINT { (X_MIN_POS + 10), (Y_MAX_POS - 10), 20 }
#define NOZZLE_PARK_XY_FEEDRATE 100
  
To:
#define NOZZLE_PARK_POINT { (X_MAX_POS + 1), (Y_MAX_POS - 1), 5 }
#define NOZZLE_PARK_XY_FEEDRATE 60  

From:
#define PRINTCOUNTER

To:
//#define PRINTCOUNTER

From:
#define SD_CHECK_AND_RETRY

To:
//#define SD_CHECK_AND_RETRY

From:
//#define FAN_SOFT_PWM

To:
#define FAN_SOFT_PWM

From:
#if ENABLED(NEOPIXEL_LED)
  #define NEOPIXEL_TYPE   NEO_GRBW // NEO_GRBW / NEO_GRB - four/three channel driver type (defined in Adafruit_NeoPixel.h)
  #define NEOPIXEL_PIN     4       // LED driving pin
  //#define NEOPIXEL2_TYPE NEOPIXEL_TYPE
  //#define NEOPIXEL2_PIN    5
  #define NEOPIXEL_PIXELS 30       // Number of LEDs in the strip, larger of 2 strips if 2 neopixel strips are used
  #define NEOPIXEL_IS_SEQUENTIAL   // Sequential display for temperature change - LED by LED. Disable to change all LEDs at once.
  #define NEOPIXEL_BRIGHTNESS 127  // Initial brightness (0-255)
  //#define NEOPIXEL_STARTUP_TEST  // Cycle through colors at startup
  
To:
  #if ENABLED(NEOPIXEL_LED)
  #define NEOPIXEL_TYPE   NEO_GRB // NEO_GRBW / NEO_GRB - four/three channel driver type (defined in Adafruit_NeoPixel.h)
  #define NEOPIXEL_PIN     4       // LED driving pin
  //#define NEOPIXEL2_TYPE NEOPIXEL_TYPE
  //#define NEOPIXEL2_PIN    5
  #define NEOPIXEL_PIXELS 3       // Number of LEDs in the strip, larger of 2 strips if 2 neopixel strips are used
  #define NEOPIXEL_IS_SEQUENTIAL   // Sequential display for temperature change - LED by LED. Disable to change all LEDs at once.
  #define NEOPIXEL_BRIGHTNESS 127  // Initial brightness (0-255)
  #define NEOPIXEL_STARTUP_TEST  // Cycle through colors at startup
  
#  Configuration_adv.h
  
From:
//#define FAN_KICKSTART_TIME 100

To:
#define FAN_KICKSTART_TIME 50

From:
#define DISABLE_INACTIVE_Z true  

To:
#define DISABLE_INACTIVE_Z false

From:
#define SD_MENU_CONFIRM_START

To:
//#define SD_MENU_CONFIRM_START

From:
#define SDCARD_SORT_ALPHA

To:
//#define SDCARD_SORT_ALPHA

From:
#define STATUS_CHAMBER_ANIM

To:
//#define STATUS_CHAMBER_ANIM

From:
//#define STATUS_HEAT_PERCENT 

To:
#define STATUS_HEAT_PERCENT 

From:
//#define BABYSTEP_ALWAYS_AVAILABLE

To:
#define BABYSTEP_ALWAYS_AVAILABLE

From:
#define LIN_ADVANCE

To:
//#define LIN_ADVANCE

From:
#define ADVANCED_PAUSE_FEATURE

To:
//#define ADVANCED_PAUSE_FEATURE

From:
#define FILAMENT_LOAD_UNLOAD_GCODES

To:
//#define FILAMENT_LOAD_UNLOAD_GCODES

All from:
#define *_CURRENT_HOME

All to:
//#define *_CURRENT_HOME

From:
//#define MONITOR_DRIVER_STATUS

To:
#define MONITOR_DRIVER_STATUS

From:
  #define X_HYBRID_THRESHOLD     100  // [mm/s]
  #define X2_HYBRID_THRESHOLD    100
  #define Y_HYBRID_THRESHOLD     100
  #define Y2_HYBRID_THRESHOLD    100
  #define Z_HYBRID_THRESHOLD       3
  #define Z2_HYBRID_THRESHOLD      3
  #define Z3_HYBRID_THRESHOLD      3
  #define E0_HYBRID_THRESHOLD     30
  #define E1_HYBRID_THRESHOLD     30
  
To:
  #define X_HYBRID_THRESHOLD     175  // [mm/s]
  #define X2_HYBRID_THRESHOLD    175
  #define Y_HYBRID_THRESHOLD     175
  #define Y2_HYBRID_THRESHOLD    175
  #define Z_HYBRID_THRESHOLD      10
  #define Z2_HYBRID_THRESHOLD     10
  #define Z3_HYBRID_THRESHOLD     10
  #define E0_HYBRID_THRESHOLD     60
  #define E1_HYBRID_THRESHOLD     60
  
From:
#define SQUARE_WAVE_STEPPING

To:
//#define SQUARE_WAVE_STEPPING

From:
//#define TMC_DEBUG

To:
#define TMC_DEBUG
