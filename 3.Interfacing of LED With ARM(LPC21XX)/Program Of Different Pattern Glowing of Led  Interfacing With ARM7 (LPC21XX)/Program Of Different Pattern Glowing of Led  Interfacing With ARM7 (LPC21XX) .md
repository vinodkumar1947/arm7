3. Program Of Different Pattern Glowing of Led  Interfacing With ARM7 (LPC21XX) 
 

	/******************************************************
IDE :- Keil
DEVELOPED BY:- embford.com
WHAT PROGRAM DO:- PROGRAM OF 3 PATTERN OF LED'S IS SHOWN 
USING ARM(LPC21XX)
******************************************************/
 
#include<lpc21xx.h>  //header file of lpc2148
 
#include<math.h>  // this function is for pow function
 
#define led_clr IO0CLR   
#define led_set IO0SET
 
void delay();  // difinion of led funtion
 
char ar[]={0x81,0x42,0x24,0x18,0x24,0x42,0x81};
 
void main()
   {
        int n,j,i;
        PINSEL0=0X00000000;   // select port0 as gpio mode
        IO0DIR=0XFFFFFFFF;    // make port0 as output mode 
        while(1)
          {
                n=2;
                while(n--)
                  {
                        for(i=0;i<8;i++)
                          {
                                led_set=pow(2,i);  
                                // pow is function defined in math.h it make power of 2 as i
                                // when i=0, pow(2,i)=1;
                                // when i=1, pow(2,i)=2;
                                // when i=2, pow(2,i)=4;
                                // when i=3, pow(2,i)=8;
                               delay();
                               led_clr=pow(2,i);
                          }
                                                                                                
                       for(i=7;i>=0;i--)
                          {
                                led_set=pow(2,i);  
                                // pow is function defined in math.h it make power of 2 as i
                                // when i=0, pow(2,i)=1;
                                // when i=1, pow(2,i)=2;
                                // when i=2, pow(2,i)=4;
                                // when i=3, pow(2,i)=8;
                                delay();
                                led_clr=pow(2,i);
                         }
                  }
                n=2;
                while(n--)
                   {
                        for(i=0;i<7;i++)
                          {
                                led_set=ar[i];
                                delay();
                                led_clr=ar[i];
                          }
                   }
                n=2;    
                while(n--)
                   {       
                        led_set=0x00;
                        delay();
                        led_clr=0x00;
                        led_set=0x01;
                        delay();
                        led_clr=0x01;
                        led_set=0x03;
                        delay();
                        led_clr=0x03;
                        led_set=0x07;
                        delay();
                        led_clr=0x07;
                        led_set=0x0f;
                        delay();
                        led_clr=0x0f;
                        led_set=0x1f;
                        delay();
                        led_set=0x3f;
                        delay();
                        led_clr=0x3f;
                        led_set=0x7f;
                        delay();
                        led_clr=0x7f;
                        led_set=0xff;
                        delay();
                        led_clr=0xff;
                
                
                        led_set=0xfe;
                        delay();
                        led_clr=0xfe;
                        led_set=0xfc;
                        delay();
                        led_clr=0xfc;
                        led_set=0xf8;
                        delay();
                        led_clr=0xf8;
                        led_set=0xf0;
                        delay();
                        led_clr=0xf0;
                        led_set=0xe0;
                        delay();
                        led_clr=0xe0;
                        led_set=0xc0;
                        delay();
                        led_clr=0xc0;
                        led_set=0x80;
                        delay();
                        led_set=0x00;
                        delay();
                        led_clr=0x00;
                
                
                
                        led_set=0x80;
                        delay();
                        led_clr=0x80;
                        led_set=0xc0;
                        delay();
                        led_clr=0xc0;
                        led_set=0xe0;
                        delay();
                        led_clr=0xe0;
                        led_set=0xf0;
                        delay();
                        led_clr=0xf0;
                        led_set=0xf8;
                        delay();
                        led_clr=0xf8;
                        led_set=0xfc;
                        delay();
                        led_clr=0xfc;
                        led_set=0xfe;
                        delay();
                        led_clr=0xfe;
                        led_set=0xff;
                        delay();
                        led_clr=0xff;
                
                
                        led_set=0x7f;
                        delay();
                        led_clr=0x7f;
                        led_set=0x3f;
                        delay();
                        led_clr=0x3f;
                        led_set=0x1f;
                        delay();
                        led_clr=0x1f;
                        led_set=0x0f;
                        delay();
                        led_clr=0x0f;
                        led_set=0x07;
                        delay();
                        led_clr=0x07;
                        led_set=0x03;
                        delay();
                        led_clr=0x03;
                        led_set=0x01;
                        delay();
                        led_clr=0x01;
                        led_set=0x00;
                        delay();
                        led_clr=0x00;
    
                   }
           }       
    }
 
void delay()  // difinion of led funtion
  {
      int i,j;
      for(i=0;i<1000;i++)
        for(j=0;j<500;j++);
  }
