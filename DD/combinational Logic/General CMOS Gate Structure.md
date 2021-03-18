- THe general form used to construct any inverting logic gate, such as: NOT, NAND, or NORs 
![[Pasted image 20210111162146.png]]

- When transistors are in parallel, the network is ON if one of the transistors is ON
- When transistors are in series, the network is ON only if all transistors are ON
 - pMOS transistors are used for pull-up
 - nMOS transistors are used for pull-down
 - Exactly one network should be ON, and the other network should be OFF at any given time
 - If both networks are ON at the same time, there is short circuit, likely incorrect operation
 - If both networks are OFF at the same time, the output is floating -> undefined