### Chinchila Scaling Law
- the relation between amount of parameters and training tokens
- training token should be ~20 times parameters


## Finetuning
#### in context learning
- does not always work for smaller models
- examples take up space in the context window

#### instruction fine-tuning
- full fine tuning updates all parameters

#### Finetuning on a singe task
- catastrophic forgetting may occur
	- reduction in ability to other tasks
- Solution
	- instruction finetune on multiple tasks
		- problems are
			- requires lots of data
	- PEFT - parameter efficient fine tuning

## LLM Evaluation Metric
- BLEU - uses for machine translation
- ROUGE - uses for text summarization
	- ROUGE1 -
		- uses unigram
		- doesnot take into account of order
	- ROUGE2
		- uses bigram
	- ROUGE-L
		- uses LCS
	- ROUGE-clipping