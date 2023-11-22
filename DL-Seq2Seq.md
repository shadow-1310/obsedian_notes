
- Many-to-One
	- sentiment classification
- one-to-many
	- music generation
	- image captioning
- many-to-many(unequal input output)
	- machine translation
	- text summarizer
	- question-answering
	- chatbot
	- speech to text 
- many-to-many (equal input output)
	- NER
	- POS tagging

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

#### Difference in GRU and LSTM
- 1st difference
	- GRU has only one state which is hidden state
		- in GRU , $h_t=C_t$
	- LSTM has 2 states hidden state and cell state and they are related as below
		- in LSTM, $h_t=o_t*tanh(C_t)$ 

- 2nd difference
	- GRU has 2 gates
		- reset gate, short term memory
		- update gate, long term memory


### Bi-directional RNN