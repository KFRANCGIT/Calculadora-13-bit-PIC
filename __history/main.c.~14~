#include <18f4620.h>
#use delay(clock=32M)
#fuses INTRC_IO, NOFCMEN, NOIESO, PUT, NOBROWNOUT, NOWDT
#fuses NOPBADEN, NOMCLR, STVREN, NOLVP, NODEBUG



void puertoDef8Bits(unsigned int8);

void main(void){

   unsigned int8 varEstados = 254;
   set_tris_b(0x00);
   setup_oscillator(OSC_32MHZ);   
  
   while(true){
      puertoDef8Bits(varEstados);
   }
      
}

void puertoDef8Bits(unsigned int8 result){
   
   // A0 A1 A2 A3 A5 E0 E1 E2 //// B2 B3 B1 B4 B0
   // Encendido de cada puerto suponiendo que A0 es el mas significativo
   if(bit_test(result,0)){
      output_high(pin_e2);
   }
   if(bit_test(result,1)){
      output_high(pin_e1);
   }
   if(bit_test(result,2)){
      output_high(pin_e0);
   }
   if(bit_test(result,3)){
      output_high(pin_a5);
   }
   if(bit_test(result,4)){
      output_high(pin_a3);
   }
   if(bit_test(result,5)){
      output_high(pin_a2);
   }
   if(bit_test(result,6)){
      output_high(pin_a1);
   }
   if(bit_test(result,7)){
      output_high(pin_a0);
   }
  
      // A0 A1 A2 A3 A5 E0 E1 E2 B2 B3 B1 B4 B0
      
      
   
}
