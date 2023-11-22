### RNN
- 

### GRU
![[Pasted image 20231122142512.png]]
- reset gate
	- it controls how the value candidate memory unit is calculated.
		- $r_t=0$ means, ignore previous memory
		- $r_t=1$ means take previous memory unit 
	- it depends on 2 variable
		- current information, $x_t$
		- previous memory unit, $h_{t-1}$
- candidate value memory content, $\tilde{h_t}$
	- depends on 3 values
		- current information
		- previous memory unit
		- reset gate
- update gate, $z_t$
	- controls how new memory content is calculated.
- 
- new memory content
### LSTM
- update Gate
- forget gate
- output gate