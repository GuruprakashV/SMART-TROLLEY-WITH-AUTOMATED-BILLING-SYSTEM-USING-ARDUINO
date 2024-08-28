# SMART-TROLLEY-WITH-AUTOMATED-BILLING-SYSTEM-USING-ARDUINO
The  Smart Trolley System manages trolley items using RFID technology, displays real-time updates on an LCD, and sends SMS notifications with product details and total amounts via a GSM module.
Overview
The RFID Smart Trolley System is a project designed to manage and track items in a trolley using RFID technology. This system is built with Arduino and includes an LCD display, GSM module for messaging, and RFID reader to handle different products. The trolley's total quantity and amount are displayed and updated in real-time based on RFID tag scans.

Components Used
Arduino Uno (or compatible board)
RFID Reader
LCD Display (LiquidCrystal_I2C)
GSM Module (SIM900)
SoftwareSerial Library (for GSM communication)
EEPROM Library (for storing data)
Features
RFID Scanning: Identifies and manages products scanned with RFID tags.
LCD Display: Shows real-time updates of scanned products, their quantities, and total amount.
GSM Messaging: Sends an SMS with the total product quantity and amount when requested.
Alarm Notification: Alerts when a product has expired.
Pin Configuration
LCD: I2C interface with address 0x27
RFID Reader: Connected via SoftwareSerial (Pins 4 and 5)
Alarm: Connected to pin A1
Libraries
LiquidCrystal_I2C: For handling the LCD display.
SoftwareSerial: For communication with the GSM module.
EEPROM: For data storage (if used).
Setup and Usage
Connect the Components: Wire up the RFID reader, LCD, and GSM module according to the pin configuration.

Upload the Code: Load the provided code onto your Arduino board using the Arduino IDE.

Initialize GSM Module: The GSM module is initialized in the Gsm_init() function. Make sure the GSM module is properly configured for SMS communication.

Start the System: Once the code is uploaded, the LCD will display "SHOW YOUR CARD". Scan RFID tags to manage items.

Check the LCD: The LCD will show real-time updates on the quantity and total amount of products in the trolley.

Send Message: Press the button connected to pin A0 to send an SMS with the product details.

Handle Expired Products: The system will alert with an alarm and a message if an expired product is scanned.

Code Functions
serial_Decimal3() and serial_Decimal31(): Helper functions for serial output formatting.
decimal3() and decimal4(): Display formatted numbers on the LCD.
Gsm_init(): Initializes the GSM module.
msg_send(): Sends a message with the product quantity and total amount.
serialEvent1(): Handles RFID data reception.
Troubleshooting
LCD Not Displaying: Check the I2C connections and address.
GSM Not Sending Messages: Ensure correct SIM card and network signal.
RFID Not Reading: Verify connections and RFID tag compatibility.
