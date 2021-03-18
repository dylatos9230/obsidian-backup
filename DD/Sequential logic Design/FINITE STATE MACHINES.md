## Introduction
- Synchronous sequential circuits can be drawn in the forms shown in the figure below
- These forms are called finite **state machines(FSMs)**
- They get their name because a circuit with k registers can be in one of a finite number (2^k) of unique states.
- An FSM has M inputs, N outputs, and k bits of state.
- An FSM consists of two blocks of combinational logic, **next state logic** and **output logic**, and a register that stores the state.
- On each clock edge, the FSM advances to the next state, which was computed based on the current state and inputs.
- There are two general classes of finite state machines, characterized by their functional specifications.
	- In [[Moore machines]], the outputs depend only on the current state of the machine.
	- In [[Mealy machines]], the outputs depend on both the current state and the current inputs.
	![[Pasted image 20210126131526.png]]
- A natural question is how to determine the [[state encoding]] that produce she circuit with the fewest logic gates or the shortest propagation delay.
- [[FSM Design Procedure]]