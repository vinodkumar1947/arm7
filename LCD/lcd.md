/******************************************************
embford.com
DEVELOPED BY:- 
WHAT PROGRAM DO:- LCD DISPLAY USING ARM7(LPC21XX)
******************************************************/

> > #include<lpc21xx.h>
> > 
> > #define LCD (0xff<<16)
> > #define RS (1<<13)
> > #define RW (1<<14)
> > #define EN (1<<15)
> > 
> > void delay_fv(unsigned int x,int y);
> > void lcd_display(unsigned int x);
> > void cmd(unsigned char m);
> > void lcd_ini();
> > 
> > int main()
> >    {
> >         PINSEL0=0X00000000;
> >         IO0DIR=0XFFFFFFFF;
> >         lcd_ini();
> >         while(1)
> >           {
> >                 lcd_ini();
> >                 lcd_display(' ');
> >                 lcd_display('W');
> >                 delay_fv(1000,400);
> >                 lcd_display('E');
> >                 delay_fv(1000,400);
> >                 lcd_display('L');
> >                 delay_fv(1000,400);
> >                 lcd_display('C');
> >                 delay_fv(1000,400);
> >                 lcd_display('O');
> >                 delay_fv(1000,400);
> >                 lcd_display('M');
> >                 delay_fv(1000,400);
> >                 lcd_display('E');
> >                 delay_fv(1000,400);
> >                 lcd_display(' ');
> >                 delay_fv(1000,400);
> >                 lcd_display('T');
> >                 delay_fv(1000,400);
> >                 lcd_display('O');
> >                 delay_fv(1000,400);
> >                 cmd(0x0c0);
> >                 lcd_display('E');
> >                 delay_fv(1000,400);
> >                 lcd_display('M');
> >                 delay_fv(1000,400);
> >                 lcd_display('B');
> >                 delay_fv(1000,400);
> >                 lcd_display('F');
> >                 delay_fv(1000,400);
> >                 lcd_display('O');
> >                 delay_fv(1000,400);
> >                 lcd_display('R');
> >                 delay_fv(1000,400);
> >                 lcd_display('D');
> >                 delay_fv(1000,400);
> >                 lcd_display('.');
> >                 delay_fv(1000,400);
> >                 lcd_display('c');
> >                 delay_fv(1000,400);
> >                 lcd_display('o');
> >                 delay_fv(1000,400);
> >                 lcd_display('M');
> >                 delay_fv(1000,400);
> >                 lcd_display('*');
> >                 delay_fv(1000,400);
> >                 lcd_display('*');
> >                 delay_fv(1000,400);
> >           }
> >    }
> > 
> > void delay_fv(unsigned int x,int y)
> >   {
> >       unsigned int i,j;
> >       for(i=0;i<x;i++)
> >       for(j=0;j<y;j++);
> >   }
> >   
> > void lcd_display(unsigned int x)
> >   {
> >      IO0CLR|=(RS|RW|EN|LCD);
> >      IO0SET|=(x<<16);
> >      IO0SET|=RS;
> >      IO0CLR|=RW;
> >      IO0SET|=EN;
> >      delay_fv(100,10);
> >      IO0CLR|=EN;
> >      delay_fv(10,10);
> >   }
> > 
> > void cmd(unsigned char m)
> >   {
> >      IO0CLR|=(RS|RW|EN|LCD);
> >      IO0SET|=(m<<16);
> >      IO0CLR|=RS;
> >      IO0CLR|=RW;
> >      IO0SET|=EN;
> >      delay_fv(100,100);
> >      IO0CLR|=EN;
> >      delay_fv(100,10);
> >   }
> > 
> > void lcd_ini()
> >    {
> >       cmd(0X38);
> >       cmd(0X0e);
> >       cmd(0X06);
> >       cmd(0X01);
> >       cmd(0X80);
> >   }