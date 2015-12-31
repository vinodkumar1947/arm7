Program Of  Led Interfacing With ARM7 (LPC2148)
 
        /****************************************************
    IDE :- Keil
    DEVELOPED BY:- embford.com
    WHAT PROGRAM DO:- PROGRAM TO BLINK LEDS CONNECTED  WITH ARM(LPC2148) CONTROLLER
    
        ******************************************************/
     
> #include<lpc21xx.h>   // header file for lpc2148 controller
> 
>  void delay();  //  initialization of delay function
>   
>  int main()
>  {
> 
> PINSEL0=0X00000000;            **// SELECT PORT0 PIN0 TO PIN 15 AS GPIO MODE**
>       
>  IO0DIR=0XFFFFFFFF;                // MAKE PORT0 PIN AS OUTPUT MODE
>       
>  while(1)
>  {
>         
>  IO0SET=0XFFFFFFFF;  // SET THE PORT0  PINS
>  delay();            // HAULT FOR SOME TIME
>  IO0CLR=0XFFFFFFFF;  // CLEAR THE PORT0 PINS
>  delay();            //HAULT FOR SOME TIME
>  }
>  }
>   
>  void delay()  **//  initialization of delay function**
> 
>  {
>  int i,j;
>  for(i=0;i<1000;i++);
>  for(j=0;j<1000;j++);
> 
>  }
> 