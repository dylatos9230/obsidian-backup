- Pick an initial value w0 randomly.
- Compute  ![[Pasted image 20210325015048.png]]
	- if Negative, increase w.
	- if Positive, decrease w.
		- hyperparameters are set by ourself:  such as learning rate
		 ![[Pasted image 20210325015314.png]]
	- Get the w1 by a substracting.
	![[Pasted image 20210325020125.png]]
- Update w iteratively.
- There may be some problems with  Gradient Descent 
	- Local minima
	- Global minnima
![[Pasted image 20210325024038.png]]