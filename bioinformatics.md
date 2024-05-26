FastQC

MultiQC

Fastp

SPAdes

Quast

BWA

SAMtools

QualiMap

FreeBayes
- Calling Variants

## Sequence Alignment
#### Scoring methods
- more penalty for transversions compared to transitions.
	- ![[Pasted image 20240526115526.png]]
- Base pairs
	- Linear gap Penalty
	- Affine Gap Penalty
		- GOP
		- GEP
- Amino acids
	- PAM250
	- BLOSUM
		- BLOSUM62
		- BLOSUM80
		- BLOSUM45
### Alignment Algorithm
- Smith-Waterman Algorithm
	- finds minimal path through dot plot
		- Similar to LCS algorithm
	- time complexity is high (N1* N2)
- BLAST - Basic Local Alignment Search Tool 
## DNAs
- made up of 4 dNTPs
- Deoxyribo-Nucleoside-Tri-Phosphate
	- Deoxyribose(Sugar)
	- Base
	- Triphosphate

## NGS
---
- DNA is collected
- it is purified
	- it is checked whether it is pure and undegraded
- RNA needs to be reverse transcribed to be sequenced.
- Library Preparation
	- collection of short dna fragments
	- cutting is done by high frequency sound wave or enzymes
- Adapter is added
	- they have index to identify 
- Successfull library is of correct size
	- high enough concentration for sequencing
- SBS - Sequence By Synthesis
	- Oligonucleotides on flow cell surface
	- Library is denatured to form single strand of DNA
	- single strands attached to oligo called forward strand 
	- reverse strand is made 
		- forward strand is washed away
- Clonal Amplification 
	- PCR at single temperature
		- Annealing - form bridge
		- Extension - strands gets copied
		- Melting - they get denatured