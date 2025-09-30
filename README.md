# ECEN5803_Project1_Module2
This is the second module for the first project containing the configurations requested using the built in STM code configurator.

CONFLICT NOTE: PA_5 is requested to be allocated as an GP output and as SCLK (alternate function). These are conflicting metods so SCLK was chosen for this pin.

CALCULATION NOTES:  
SYSCLK IS 84 MHZ  
APB2 (PCLK2) IS 5.25 MHz  

ADC------------------------------------------------------------------------  
	5.25 MHz input  
	2.625 MHz after 1/2 pre-scaler  
	101 kHz from:  
		8 bit mode (11 cycles conversion)  
		15 cycle sample time  
		26 cycles from above (11 conversion + 15 sample) cycles  
	IN4 used to be conflict free with rest of settings  

SPI------------------------------------------------------------------------  
Match clock phase and polarity to SPI 2  
	High Polarity  
	1 edge  
Clock  
	5.25 MHz input  
	82.03 kHz from 1/64 prescaler  
CS  
	Software used  
	Attached manually to PB6  
	
I2C------------------------------------------------------------------------  
Pretty much all default here to allow 100kHz and pin mapping requested  
Treated as master  

Debug------------------------------------------------------------------------  
I turned on SWD for use with STLink  
<img width="1146" height="830" alt="image" src="https://github.com/user-attachments/assets/b7264c94-7fe7-4423-ab75-9b345ee3fd0b" />

<img width="736" height="805" alt="image" src="https://github.com/user-attachments/assets/cc2d7995-faf7-4501-88e0-80257b07f73c" />
