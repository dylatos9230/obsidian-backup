 
https://www.youtube.com/watch?v=stM8dgcY1CA
- MOSFETs sandwich consists of a conducting layer called the gate on top of an insulating layer of silicon dioxide(SiO2) on top of the silicon wafer, called substrate. 

#### There are two flavors of MOSFETs: [[nMOS]] and [[pMOS]]
![[Pasted image 20210111131326.png]]
- The voltage at the gate (g) regulates the flow of current between the source (s) and drain (d). [[nMOS]] transistors are OFF when the gate is 0 and ON when the gate is 1. [[pMOS]] transistors are just the opposite: ON when the gate is 0 and OFF when the gate is 1.
- Unfortunately, MOSFETs are not perfect switches. In particular, nMOS transistors pass 0's well but pass 1's poorly. Specifically, when the gate of an nMOS transistor is at Vdd, the drain will only swing between 0 and Vdd - Vt.

 Input  | output 
 ------ | ------- 
 Low     |  Low 
 High    |  High      

- Similarly, pMOS transistor pass 1's well but 0's poorly.

 Input  | output 
 ------ | ------- 
 Low     |  High 
 High    |  Low   
 
![[Pasted image 20210111145033.png]]

#### [[CMOS]]
- To build both flavors of transistors on the same chip, manufacturing processes typically start with a p-type wafer, then implant n-type regions called wells where the pMOS transistors should go. These processes that provide both flavors of transistors are called Complementary MOS or [[CMOS]]
- In summary, [[CMOS]] processes give us two types of electrically controlled switches
