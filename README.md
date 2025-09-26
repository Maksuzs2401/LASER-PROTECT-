# LASER OVER-CURRENT PROTECTION CIRCUIT 
Laser over current protection circuit specifically designed for quantum cascade lasers
This circuit allows real time monitoring of the current flowing through the laser diode, It includes Arduino nano board to monitor the isense pins constantly. The circuit uses external ADC as the NANO’s ADC is 10-bit and it does not provide enough resolution for our implementation. It uses ADS1115 to monitor Isense pins and transfer data over to NANO via I2C protocol. 
MLD203CHBE has an internal 1 Ohm resistor connected across Isense+ and Isense- pins so that the voltage across pins is directly related to the current flowing through the laser diode.
The gate pin of the nMOS is driven by the digital pin of NANO. In over current condition the mosfet cuts off the laser diode from the circuit.
The OLED display shows the real time reading of the current flowing through the laser  diode.
With the help of an external push button the circuit can be reset back to normal operation after current drops down to the normal level. 
