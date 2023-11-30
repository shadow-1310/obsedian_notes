## Concatenate vs Stack
- concatenate
	- joins a sequence of tensors along an existing axis
	- e.g. convert images in different batch to a single batch
- stack
	- joins a sequence of tensors along a new axis
	- e.g. convert individual images to a batch

### seed
- we can reproduce the result 

#### Defining a custom module
- must subclass torch.nn.module
#### Methods
- __init__
	- initialize the parent class (super.__init__)
	- define all the params
- forward method
	- define how it will forward propagate


- namedtuple
	- name each index in the tuple
	- each element can be called by custom_tuple.

### Reflection Padding
