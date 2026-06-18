# Led-Matrix-Display
This is a custom Smart LED matrix display system built using ESP32 and HUB75 RGB matrix. Its has many modes like clock, text, animation which can be controlled by the user.

## Why I Made It
I have always enjoyed building things and learning by creating. When I came across HUB75 LED matrix displays, they seemed both interesting and challenging, which made me want to explore them further.

Matrix Clock V1 was created as a way to learn more about electronics, PCB design, firmware development, and product design while building something useful and fun.
### Zine
<img width="1410" height="2000" alt="Matrix Clock v1" src="https://github.com/user-attachments/assets/c7d995b6-a9da-44ab-92b9-d96d021f93ec" />

# CAD render
<img width="645" height="402" alt="Opera Snapshot_2026-06-14_113301_cad onshape com" src="https://github.com/user-attachments/assets/561361ad-7791-457b-8ebc-848961ff9c45" />

[Cad source](https://cad.onshape.com/documents/1d3eda01ccfd42c3370510ad/w/1b34d9f3683c544fbe63b600/e/64e58fe6b530831de16bd061?renderMode=0&uiState=6a33ac866645666a43711704)

# PCB Screenshots
<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/f24f9a25-e176-4a98-af34-6d013d499f43" />
<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/26eb5514-4b54-4024-9364-6607d50b13df" />

# Overview
Matrix Clock V1 is a compact embedded display platform built around an ESP32 and a 64×32 HUB75 LED matrix panel.
The project combines hardware design, PCB design, firmware development, and enclosure CAD into a single integrated system.

# Features
- Real time Clock display
- Multiple display modes
- Button based control
- RTC timekeeping

# System design
See detailed system design in ' docs/architecture.md '.

# Hardware Components
- ESP32 Devboard
- HUB75 RGB matrix
- RTC module
- Buttons
- Custom PCB

# How to Build one of your own

If you would like to build your own Matrix Clock V1, the general process is fairly straightforward.

### 1. Order the Components
Use the BOM provided in this repository to source all required components, including:

* ESP32 DevKit
* HUB75 LED Matrix
* DS3231 RTC Module
* Push Buttons
* Connectors and Headers
* Custom PCB

### 2. Manufacture the PCB
Export the Gerber files from the PCB folder and upload them to your preferred PCB manufacturer.
Once the boards arrive, inspect them for any manufacturing defects before assembly.

### 3. Assemble the Hardware
Solder the required headers, connectors, and sockets onto the PCB.

Then connect:

* ESP32 DevKit
* RTC Module
* HUB75 Display
* External Push Buttons

Double-check all wiring and polarity before applying power.

### 4. Upload the Firmware
Open the firmware project in the Arduino IDE.
Install the required libraries and upload the firmware to the ESP32.
Once uploaded, verify that:

* The display initializes correctly
* The RTC is detected
* The buttons function as expected

### 5. Assemble the Enclosure
3D print the enclosure files located in the CAD folder.
Mount the display, PCB, and buttons into the enclosure and secure all components.

### 6. Power On
Connect a suitable 5V power supply and power up the system.
The display should start in Clock Mode and can be controlled using the external buttons.

# Status
In designing phase.

# License
This project is licensed under the MIT License.

## Author
Pranay Kamle
Matrix Clock V1 • 2026
