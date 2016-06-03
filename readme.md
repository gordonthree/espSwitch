ESP8266 Dual DC Switch

WiFi connected switch designed for moderate current low voltage DC loads using the Espriff ESP8266 SoC module. I’m using an ESP07 module for external antenna. support and the TC4427 gate drive IC to drive the mosfets hard using input voltage (up to 18v). Any D-PAK N-fet should work, just watch Vgs vs Ids.

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

