
### Problem Statement
---
Given a passage as input, A NLP model should output list of MCQs where each question can have multiple answers

### File description
---
- scipt.py
	- this python file contains all the methods and classes to generate the MCQ given a context
- documentation.md
	- A markdown file describing the workflow and required libraries
- requirements.txt
	- dependencies for the script.py

### Major open-source NLP models/libraries used
----
#### Hugging face transformers
- Google Flan-T5 for tokenizer
- [Parth/result](https://huggingface.co/Parth/result)
	- A custom trained transformer model shared on Hugging Face
	- this model takes 2 inputs, context and answer/keyword and returns a probable question on that

#### NLTK library
this library was used for its various corpuses
- in this project corpuses used are "brown" and "stopwords" corpus

#### Sense2Vec
- this module was used for generating distractors as options 
- this is the link to project site [github page](https://github.com/explosion/sense2vec)

#### pke (Python Keyphrase Extraction module)
- this module was used for extracting the keywords which will generate the MCQ
- this is the link to project site [github page](https://github.com/boudinfl/pke)

### FlashText
- this library is used in this project to find phrases containing given keyword so that we can do a mapping of keyword to sentences late to be feed into the transformer model
- this is the link to project site [github page](https://github.com/vi3k6i5/flashtext)

### Workflow
---
1. Getting Keywords and their corresponding phrases
	- keywords are extracted using "pke" module
	- and their corresponding phrases are extracted using "flashtext" module
- Checking if distractor available for keyword
	- all the extracted keywords are passed into sense2vec library to check if equal or greater than 4 distractor are available or not.
	- If not then these keywords are rejected 
- keyword and corresponding sentences are mapped into the required format of the model
- keyword_sentence_mapping are converted to embeddings using google-flan-t5 encoder
- the embedding are passed into the model for question generation.
- finally the distractors along with the question are wrapped into required format.