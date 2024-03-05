## Resources
- [original paper](https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf)
- [Umar Jamil youtube](https://www.youtube.com/watch?v=bCz4OMemCcA&t=16s)
- [J Alammar blog](https://jalammar.github.io/illustrated-transformer/)
### Positional Encoding
- to change the embeddings based on the position of the word
- calculated once initially and not trained
- we can get positional embeddings by doing a sum of word embedding and positional vectors
### Self Attention
- Properties
	- Permutation invariant
		- interchanging position of 2 words in the input will also change the position in the output exactly same. It will not alter the values.
	- values along the diagonal is the highest in attention matrix 
#### Single Headed
$$Attention(Q,K,V)=softmax(\frac{QK^T}{\sqrt{d_k}})V$$

#### Multihead
$$Multihead(Q,K,V)=concat(head_1,head_2,...,head_h)W^O$$
$$where,\;head_i=Attention(QW_i^Q,KW_i^K,VW_i^V)$$