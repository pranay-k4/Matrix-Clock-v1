# The Bill of the Materials required v1 : ( Will be updated later )
## 1) ESP32 Dev board 
- Quantity : 1
- Avg price ~ 5$
- Distributor:  Robu, Amazon.
## 2) HUB75 Led Matrix display 32x64
- Quantity : 1
- Avg price ~ 6$
- Distributor: ALIEXPRESS.
## 3) RTC Module 
- Quantity : 1
- Avg price ~ 1-1.5$
- Distributor : Robu, Amazon
## 4) Push Button 19mm
- Quantity : 2
- Avg price ~ 1-1.5$
- Distributor : Robu, Amazon
## 5) PCB 
- Quantity : 1
- Making Price : 2$
- Shipping : 9$
- Distributor : JLCPCB

### Note
- This will be updated as there will some other minor component needed.
- Also the custom PCB will be added later soon



# Bill of Materials (BOM) – Matrix Clock v1 (Rev A)

| Item No. | Component Name              | Description / Specs                          | Qty | Package / Footprint                  | Notes                              | Link | Unit Price | Total |
|----------|----------------------------|----------------------------------------------|-----|-------------------------------------|------------------------------------|------|------------|-------|
| 1        | ESP32 DevKit (30-pin)      | ESP32-WROOM Dev Board, 30-pin                | 1   | PinSocket_1x15_P2.54mm x2           | Main controller                    |      |            |       |
| 2        | HUB75 LED Matrix Panel     | 64x32 RGB LED Matrix (HUB75)                 | 1   | External                            | Display module                     |      |            |       |
| 3        | RTC Module (DS3231)        | Real Time Clock Module                       | 1   | PinHeader_1x04_P2.54mm              | Timekeeping                        |      |            |       |
| 4        | Screw Terminal (Power In)  | 2-pin, 5.08mm pitch                          | 1   | TerminalBlock_2P_5.08mm             | Main power input                   |      |            |       |
| 5        | Screw Terminal (HUB75 PWR) | 2-pin, 5.08mm pitch                          | 1   | TerminalBlock_2P_5.08mm             | Power to LED matrix                |      |            |       |
| 6        | HUB75 Header               | 2x8 Pin Header, 2.54mm pitch                 | 1   | PinHeader_2x08_P2.54mm              | Data connector                     |      |            |       |
| 7        | Button Connector Header    | 1x04 Pin Header, 2.54mm                      | 1   | PinHeader_1x04_P2.54mm              | External buttons                   |      |            |       |
| 8        | Female Headers (ESP32)     | 1x15 Pin Socket, 2.54mm                      | 2   | PinSocket_1x15_P2.54mm              | ESP32 mounting                     |      |            |       |
| 9        | External Push Buttons      | Momentary Push Button (12mm / 16mm)          | 2   | Panel Mount                         | Mode / Control buttons             |      |            |       |
| 10       | Jumper Wires / Dupont      | Female-Male / Female-Female wires            | As needed | N/A                            | Wiring connections                 |      |            |       |
| 11       | Power Supply               | 5V, ≥5A DC Adapter                           | 1   | External                            | Main power source                  |      |            |       |
| 12       | Mounting Hardware          | M3 Screws + Standoffs                        | As needed | MountingHole_3.2mm             | PCB mounting                       |      |            |       |
| 13       | PCB                        | Custom PCB (Gerber Manufactured)             | 1   | Custom                              | Main board                         |      |            |       |

---

## Notes

- Ensure all headers are **2.54mm pitch** unless otherwise specified  
- Use **momentary (not toggle)** buttons  
- Power supply should handle **HUB75 current (~4–5A recommended)**  
- Verify connector orientation before soldering  
