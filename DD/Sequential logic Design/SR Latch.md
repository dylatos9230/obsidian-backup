## Introduction
- The SR latch is composed of tewo corss-coupled NOR gates
- Its state can be controlled through the S and R inputs, which **set** and **reset** the output Q
## Schematic
![[Pasted image 20210120023501.png]]
## Truth Table 
![[Pasted image 20210120023534.png]]
## Symbol
![[Pasted image 20210120023645.png]]
## Property
- The SR latch is a bistable element with one bit of state stored in Q
- However, the state can be controlled through the S and R inputs
- When R is asserted, the state is reset to 0
- When S is asserted, the state is set to 1.
- When neither is asserted, the state retains its old value.
- The entire history of inputs can be accounted for by the single state variable Q.
- No matter what pattern of setting and resetting occurred in the past, all that is needed to predict the future behavior of the SR latch is whether it was most recently **set** or **reset**
## Evolution
