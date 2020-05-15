# GcodeCNC_SD_OLED_JOYSTICK
For a CNC 3 axis. Reads 1 (of 4) Gcode files from SD card an execute it. 
  Does JOGs, Home, Zero Piece, CALIB_Z, ...

This code includes a mix of GcodeCNCDemo4AxisRAMPS (without arcs) and arcs from GcodeCNCDemo4AxisV2 
You can find the originals codes at : https://github.com/MarginallyClever/GcodeCNCDemo 

My code is written for a Arduino MEGA , with or without a RAMPS.
- Minimum hardware add : an SD card reader it will read a default Gcode an execute it at power up.
  ( 4 lines of code to change )

- additional hardware : (all tests where made so, with NEMA23, µStepper drivers (1 to 4 µ steps), no RAMPS) :
  OLED 128x64, (don't forget to adapt the library)
  joystick, 
  “acknowledge” button (can be the push button from the joystick if you can push it in the axis while making a jog...) ,
  red push button to save ZERO_PIECE in EEPROM and is also a ”PAUSE/RESTART” (freezes, goes to safe_Z,…, then down and continue),
  end switches : for the “HOME” or “MY_ZERO” (during a work, hitting one freezes everything…),
  a few leds.

At the end of the main void there is a "ReadMe" more complete than this.  
