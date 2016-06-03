ESP8266 Dual DC Switch

WiFi connected switch designed for moderate current low voltage DC loads using the Espriff ESP8266 SoC module. I’m using an ESP07 module for external antenna. support and the TC4427 gate drive IC to drive the mosfets hard using input voltage (up to 18v). Any D-PAK N-fet should work, just watch Vgs vs Ids.

Bare PCB can be ordered from OSH Park: <https://www.oshpark.com/projects/4C8Vl9AT>

PROG Header: On the back side of the PCB, there are pads for 0603 size pull-up resistors (to the 3v3 rail) near the "PROG" header. Once loaded with OTA software, the ESP firmware can be configured to use these ports as either an I2C or Dallas One-Wire port. A small solder jumper is available to connect / disconnect the pull-ups from 3v3 if nessecary to reflash the ESP via serial port.

PRG Header: One pad is ESP GPIO0, the other pulled down to gound via a 1k resistor. Jumper these pads prior to power-up to force ESP into serial port flash mode. 

Current BOM:

ESP8266 ESP07 Module

IC1 TC4427 (IR4427) Gate Drive IC from Microchip, SO8

IC2 Generic LDO voltage regulator, 3.3v output, SOT-223

Q1, Q2 MOSFETs N-channel, logic level, TO-252 DPAK

D1, D2 Schottky Diode, 3a, 40v, SOD-123

S1, S2 Optional, SMT LED, 0603

CIN, COUT 4.7-10uF ceramic, X7R, low-esr, CIN rated voltage 2x Vin, 1206

C1 100nF ceramic, X7R, low-esr, 0603

C2 220-470uF tantalum, 6.3v, tank capacitor for esp radio, Case size D

RDV1, RDV2 optional, 0.5% recommended precision resistor for voltage divider, adjust values as needed to achieve 1v output at max input voltage, 0603

R* various resistors, values as indiciated, 0603

PROG, PRG Do not populate, holes are spaced to hold onto a pin header temporarily for programming
