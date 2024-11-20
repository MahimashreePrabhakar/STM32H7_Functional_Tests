# STM32H7_Functional_tests
contains the  for the STM32H753ZI nucleo board tests
# Prescaler calculations
Sysclk = 64 MHz = Fapb <br />
PWM Freq = 115 Hz <br />
Timer freq = 29,425 Hz  <br />
## Formulas 

Period or ARR = 255 <br />


$$Ftimer = \frac{\text{Fapb}}{\text{PRESCALER+1}}$$

$$Fpwm = \frac{\text{Ftimer}}{\text{ARR+1}}$$

Therefore, the prescaler can be calculated by:

$$PRESCALER = \frac{\text{Fapb} }{\text{(ARR+1)}\cdot \text{Fpwm}}-1$$

For the specific example:

ARR = 255 (this gives 256 timer ticks per PWM period)<br />
Prescaler = 2174 <br />
