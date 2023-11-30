## Concatenate vs Stack
- concatenate
	- joins a sequence of tensors along an existing axis
	- e.g. convert images in different batch to a single batch
- stack
	- joins a sequence of tensors along a new axis
	- e.g. convert individual images to a batch

### seed
- we can reproduce the result 

Squeeze vs unsqueeze
- squeeze
	- remove a redundant dimension
- add a dimension

Tensor.t and Tensor.transpose
- tensor.t -> only 2 dimension
	- returns non contiguous array
- tensor.transpose -> for any dimension

contiguous vs non contiguous
- non-contiguous
	- next element in the same dimension is not in next contiguous memory location
	- tensor.is_contiguous(), also can be find out by tensor.stride()
	- operations returning nc
		- view
		- narrow
		- expand
		- transpose
- contiguous
	- next element in the same dimension is in next contiguous memory location

reshape vs view
- view
	- view uses the original object, doesnot create new memory object
	- only applicable for contiguous tensor.
- reshape
	- reshape doesn't guarantee that
	- can be applied to anything
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
