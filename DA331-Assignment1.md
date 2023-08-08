## Questions - to be done using Hadoop map-reduce architecture
---
### **Q1 - Implement Simple page rank** -  A Page Ranking System on normal inward link summation strategy
#### Approach

### Q2 - Implement page rank using 4 different strategy
#### approach 1: The flow model
reference: 
	[Lecture 6 — PageRank The Flow Formulation | Stanford University - YouTube](https://www.youtube.com/watch?v=1nLV8FEaZD0)
	[noc19-cs33 Lec 31 PageRank Algorithm in Big Data - YouTube](https://www.youtube.com/watch?v=k3KryL5XJaA)
![[Pasted image 20230806153437.png]]
- first consider all nodes have equal importance
- then in 2nd iteration recalculate page rank based on the summation of  input link
#### **approach 1- errors**:
- getting the error
	- INFO mapreduce.job: Job job_local_756262378_001 failed with state FAILED due to: NA

#### approach 2: add damping factor
reference: 
![[Pasted image 20230806153820.png]]

#### approach 3: 