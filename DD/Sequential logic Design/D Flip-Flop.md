## Introduction
- A **D flip-flop** can be built from two back-to-back D latches controlled by complementary clocks
	1. The frist latch, L1, is called the **master**.
	2. The second latch, L2, is called the **slave**.
	3. The node between them is named N1.
## Schematic
![[Pasted image 20210121014330.png]]
## Symbol
![[Pasted image 20210121014348.png]]
## Condensed Symbol
![[Pasted image 20210121014415.png]]

## Property
- When CLK = 0, the master latch is transparent and the slave is opaque.
	- Therefore, whatever value was at D propagates through to N1.
- When CLK = 1, the master goes opaque and the slave becomes transparent
	- Even if the value at N1 propagates through to Q, N1 is cut off from D.
- Hence, whatever value was at D immediately before the clock rises from 0 to 1 gets copied to Q immediately after the clock rises.
- At all other times, Q retains its old value, because there is always an opaque latch blocking the path between D and Q.
- In other words, a D flip-flop copies D to Q on the **rising edge of the clock**, and remembers its state at all other times.
	- The rising edge of the clock is often just called the **clock edge** for brevity.
	- The clock edge indicates when the state should be updated
	- A D flip-flop is also known as a **master-slave flip-flop**, an **edge-triggered flip-flop**, or a positive **edge-triggered flip-flop**.