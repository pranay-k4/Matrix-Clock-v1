# Firmware Plan
Here I will disscuss the how the firmware will work and the display modes.

## Main system Loop
In main system loop the ESP32 will perfom these following task :
- Take Input from the Button.
- Take the time data from the RTC module.
- Display Rendering
- Refesh the HUB75 Led Matrix display.

## Button UI
For the user interface I plan to add to button with the following features:
- Button 1:
  - When pressed changes the display modes.

- Button 2:
  - When pressed changes the brightness
  - When pressed and hold it turns off and on the system.
 
## Display Modes
There will be following display modes:
- Clock display mode
- Custom Text
- Animation display

