# Lift-desk-ESPHome-controller
Firmware for automating a lifting desk based on the ESP32-C6 and ESPHome. The project allows you to integrate a standard push-button desk into a smart home system via Thread.

**Features**

• Bidirectional control: Simulates physical button presses (Up, Down, Presets 1-3).

• OpenThread support: Works in modern mesh networks (FTD - Full Thread Device).

• Home Assistant integration: Automatic detection via Native API.

• "Cover" device type: The table appears as a curtain/blind, allowing for convenient height control.

• Height sensor ready (not finished): Working with the VL53L0X ToF sensor for precise positioning in centimeters.

**Hardware**
• Microcontroller: ESP32-C6-DevKitC-1.
• Sensor (optional): VL53L0X (for height measurement).
• Peripherals: Optocouplers for closing contacts on the desk's standard remote control.

**Operating Logic**

The firmware uses the template platform to create the Cover entity.

• Open: Closes the "Up" relay.

• Close: Closes the "Down" relay.

• Stop: Opens both relays.

• Presets: Separate buttons in the interface for quickly switching to saved table positions.
