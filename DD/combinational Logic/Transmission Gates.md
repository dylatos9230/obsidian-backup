## Introduction
- Designers find it convenient to use an ideal switch that can pass both 0 and 1 well.
- nMOS transistors are good at passing 0 and pMOS transistors are good at passing 1, so the parallel combination of the two passes both values well.
## Schematic
![[Pasted image 20210122175716.png]]
## Property
- The two sides of the switch are called A and B because a switch is bidirectional and has no preferred input or output side.
- The control signals are called enables, EN and complementary of EN respresented by symbol !EN.
- When EN = 0 and !EN = 1, both transistors are OFF. Hence, the transmission gate is OFF or disabled, so A and B are not connected.
- When EN = 1 and !EN = 0, the transmission gate is ON or enabled, and any logic value can flow between A and B.