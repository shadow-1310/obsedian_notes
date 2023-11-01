### LDA - Latent Dirichlet Allocation, 
[serrano part1](https://www.youtube.com/watch?v=T05t-SqKArY)
[serrano part2](https://www.youtube.com/watch?v=BaM1uiCpj_E)
![[Pasted image 20231101105551.png]]
- we choose different random setting and generate fake documents, the setting which maximizes probability of getting the original document is chosen
	- Dirichlet distribution
		- alpha
			- alpha = 0, uniform distribution
			- alpha < 1, points make different groups
			- alpha > 1, points stick together
		- geometry shapes
			- 2 topic - line
			- 3 topics - triangle
			- 4 topics - tetrahedron, 
				- not square because distance from pt1 to pt3(diagonal) is different
			- n-topics - n-dimensional simplex
	- Gibb's Sampling
	- [ritvik](https://www.youtube.com/watch?v=7LB1VHp4tLE)
		- articles are as monochromatic as possible - is mostly of one topic
		- words are as monochromatic as possible - means mostly one topic in all documents