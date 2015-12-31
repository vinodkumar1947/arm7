/******************************************************
IDE : - Keil
DEVELOPED BY:- embford.com
WHAT PROGRAM DO:- COUNT 000 TO 999 ON 7 SEGMENT COMMON 
CATHODE USING ARM(LPC2148)
******************************************************/


#include<LPC21XX.H>

void delay();

int ar[10]={0xc0,0xf9,0xa4,0xb0,0x99,0x92,0x82,0xf8,0x80,0x90 };
int ar1[10]={0xc000,0xf900,0xa400,0xb000,0x9900,0x9200,0x8200,0xf800,0x8000,0x9000 };
int ar2[10]={0xc00000,0xf90000,0xa40000,0xb00000,0x990000,0x920000,0x820000,0xf80000,0x800000,0x900000 };

int main()
  {
      unsigned int i,j,k;
      PINSEL0=0X00000000;
      IO0DIR =0Xffffffff;
      while(1)
        {
            for(i=0;i<10;i++)
              {
                 IO0SET =ar[i];        
                 for(j=0;j<10;j++)
                    {
                         IO0SET =ar1[j];        
                         for(k=0;k<10;k++)
                            {
                                IO0SET =ar2[k];
                                delay();
                                IO0CLR =ar2[k];
                            }
                         IO0CLR =ar1[j];
                    }
                 IO0CLR =ar[i];
             }
        }
      return 0;
   }

void delay()
   { 
      unsigned int m,n;
      for(m=0;m<500;m++)
         for(n=0;n<1000;n++);
   }