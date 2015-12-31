7 segment display  interfacing with arm7 ( lpc2148)
 

•	What is 7-SEGMENT DISPLAY (SSD)? – A seven-segment display is a form of electronic display device for displaying decimal numbers (and some alphabets too). SSD may use a liquid crystal display (LCD), a light-emitting diode (LED) for each segment, or other light-generating or controlling techniques such as cold cathode gas discharge, vacuum fluorescent, incandescent filaments, and other.
 
•	 Types of SSD– There are mainly two types of SSD available. In a simple LED package, typically all of the cathodes (negative terminals) or all of the anodes (positive terminals) of the segment LEDs are connected and brought out to a common pin; this is referred to as a “common cathode” or “common anode” device. Besides this, there is also a SSD multiplexer is used called 2 digit, 3 digit and so on as you can see on photos.
 
 
•	Operation – In a simple LED package common cathode SSD, there has 10 pin out of which 2 is ground and rest is LED segments . Particular LED segment is glow(ON) by giving logic ‘1’ to it and rests at logic ‘0’.
So we need to program this 8 pin to display our number on SSD. In following table, we convert this 8 pin’s 8 bit binary data into hex code and shows the hex code of displaying digits below.
![Capture.JPG](C:/Users/home/Desktop/Capture.JPG "")
 
•	Applications-  SSD is widely use in digital clocks, pricing menu at petrol pump, in metros and electronics meters as shown above.

