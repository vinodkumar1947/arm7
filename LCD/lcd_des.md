lcd  interfacing with ARM7 ( LPC2148 )

•	What is LCD ?-   A liquid-crystal display (LCD) is a flat panel display that uses the light modulating properties of liquid crystals. Liquid crystals do not emit light directly.
 
•	About & Types of LCD-    LCDs allow displays to be much thinner than cathode ray tube (CRT) technology. LCDs consume much less power than LED and gas-display displays because they work on the principle of blocking light rather than emitting it. An LCD is of two types depending upon how they made with either a passive matrix or an active matrix display display grid. Besides this LCD are divide in colors (blue, red, green, etc) and its display system (like 16×1, 16×2, 16×4, etc).
 
1.	The passive matrix LCD has a grid of conductors with pixels located at each intersection in the grid. A current is sent across two conductors on the grid to control the light for any pixel. Some passive matrix LCD’s have dual scanning, meaning that they scan the grid twice with current in the same time that it took for one scan in the original technology.
2.	An active matrix has a transistor located at each pixel intersection, requiring less current to control the luminance of a pixel. For this reason, the current in an active matrix display can be switched on and off more frequently, improving the screen refresh time (your mouse will appear to move more smoothly across the screen, for example). The active matrix LCD is also known as a thin film transistor (TFT) display.
 
However, active matrix is still a superior technology.
 
•	Operating parameters – below is pin description of LCD module
 
 Pin No	 Function	 Name
1	Ground (0V)	Ground
2	Supply voltage; 5V (4.7V – 5.3V)	 Vcc
3	Contrast adjustment; through a variable resistor	 VEE
4	Selects command register when low; and data register when high	Register Select(RS)
5	Low to write to the register; High to read from the register	Read/write(RW)
6	Sends data to data pins when a high to low pulse is given	Enable(E)
7	8-bit data pins	DB0
8		DB1
9		DB2
10		DB3
11		DB4
12		DB5
13		DB6
14		DB7
15	Backlight VCC (5V)	Led+
16	Backlight Ground (0V)	Led-(GND)
 	 	 
 
 
•	Applications- LCDs are used in a wide range of applications including computer monitors, televisions, instrument panels, aircraft cockpit displays, and signage. They are common in consumer devices such as video players, gaming devices, clocks, watches, calculators, and telephones, and have replaced cathode ray tube (CRT) displays in most applications. They are available in a wider range of screen sizes than CRT and plasma displays.

