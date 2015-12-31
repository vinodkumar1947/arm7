    Program Of Alternate glowing  of  Led  Interfacing With ARM7 (LPC2148)
    /******************************************************
    IDE :- Keil
    DEVELOPED BY:- embford.com
    WHAT PROGRAM DO:- PROGRAM OF ALTERNATE LEDs GLOW 
    CONNECTED TO ARM(LPC21XX)
    ******************************************************/
 
>     #include<lpc21xx.h> // header file for lpc2148 controller
>      
>     void delay();  //  initialization of delay function
>      
>     int main()
>        {
>             PINSEL0=0X00000000; // SELECT PORT0 PIN0 TO PIN 15 AS GPIO MODE
>             IO0DIR=0XFFFFFFFF; // MAKE PORT0 PIN AS OUTPUT MODE
>             while(1)
>               {
>                     IO0CLR=0X55555555; 
>                     IO0SET=0XAAAAAAAA;  // SET THE PORT0  PINS
>                     delay();            // HAULT FOR SOME TIME
>                     IO0CLR=0XAAAAAAAA;  // CLEAR THE PORT0 PINS
>                     IO0SET=0X55555555;
>                     delay();            //HAULT FOR SOME TIME
>               }
>        }
>     