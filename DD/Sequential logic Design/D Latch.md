## Motivation
- To solve the problem that lossing the time information of **when** the state should change
## Introduction
- The D latch has two inputs,
	1. The **D**, data input, controls what the next state should be.
	2. The **CLK**, clock input, controls when the state should change.
## Truth Table
![[Pasted image 20210121004703.png]]
## Schematic
![[Pasted image 20210121005440.png]]
## Symbol
![[Pasted image 20210121005502.png]]

## Property
- The CLK controls when data flows through the latch
	1. When **CLK** = 1, the latch is **transparent**. The data at D flows through to Q as if the latch were just a buffer.
	2. When **CLK** = 0, the latch is **opaque**. It blocks the new dasta from flowing through to Q, and Q retains the old value.
- So the D latch is some times called a **trasparent** latch or a **level-sensitive** latch.
- The D latch update its state continuously while **CLK** = 1.
## Evolution
