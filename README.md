# Introduction

This aims to be a sample project to get started with the Waveshare ESP32-4.3 LCD Screen.
Also includes basic wifi_setup() function to enable a WiFi connection without much effort.
If you don't need the wifi connection, just remove the wifi_setup function again.
The Arduino-CLI / Arduino-IDE should be used for this example.

// For Reference -> https://www.waveshare.com/wiki/ESP32-S3-Touch-LCD-4.3#Arduino_2

# Required Steps

    - First install the Arduino IDE
    - Extract and copy the S3-4.3-libraries into your Arduino Library folder
    - Add the following external board to your board manager via "Preferences->Additional Board URLS"
        - https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
    - Inside Arduino IDE you'll have to set the following parameters:
        - Flash Size to 8MB
        - PSRAM to OPI PSRAM

You should now be able to compile and upload the sketch.

# Further Tips

To design a fast and beautiful UI you can use SquareLine. 
You'll have to set the extension in Squareline to Arduino. 
After you designed your UI, you can export them. If you set the export path to your Arduino IDE Library path, you can use the ui directly inside your sketch.

For this you'll have to import the "ui.h" and call the ui_init() function inside your setup()

## IMPORTANT
If you receive the error, that the screen_init function could not be found, do following:
    - Navigate inside the exported ui folder
    - find the screen folder
    - copy the screen.c one folder up
    - edit the screen.c file and fix the import path from "../ui.h" to "ui.h"

Now you should be good to go!
