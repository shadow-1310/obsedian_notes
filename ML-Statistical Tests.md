
##### [Statistics made easy ! ! ! Learn about the t-test, the chi square test, the p value and more - YouTube](https://www.youtube.com/watch?v=I10q6fjPxJ0)

| data type           | test                     |
| ------------------- | ------------------------ |
| 1-categorical       | 1-sample proportion test |
| 2-categorical       | chi-squared test         |
| 1-numeric           | t-test                   |
| 2-numeric           | corelation test          |
| numeric-categorical | t-test(2-class) or ANOVA(more than 2-class)          |

- for one numeric, we are comparing against historical data to see if current sample statistic like mean, variance different than previous

##### p-value
- given the null hypothesis, the probability of seeing the current distribution
- given the null hypothesis, probability of getting sample as or more extreme as our own sample. 
### t-tests
- it is called student's t-test because the original paper was published in the pseudo name of STUDENT, author's actual name was Gosset
[T-test, ANOVA and Chi Squared test made easy](https://www.youtube.com/watch?v=ijeEYFnS2v4)
Assumptions
- normal distribution in sample and population
- same variance
- datapoints
	- same number
	- 20-30 (in this range), for 30+ use Z-test
- how to do calculation
	- [youtube video](https://www.youtube.com/watch?v=pTmLQvMM-1M)
- One sample t-test
	- compare sample with known reference
- Independent Sample t-test
	- two-tailed
		- asking if there is a difference
	- one-tailed
		- asking if difference is x in left or right is statistically significant
- paired sample t-test
	- measured values are available in pairs, i.e same person is subjected to different measurements, checking if diet plan have effect weight
	- checking in same samples from different timeline where we have overlap

### Z-test
calculate p-value in context of Z-test
<iframe width="560" height="315" src="https://www.youtube.com/embed/xHTMjxx14sU?si=Q-yxznKQXbRAiX5Y&amp;start=1641" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
- for sample size < 30, we can't assume sample variance = population variance
Approaches
- rejection region approach
	- don't have idea how strong the evidence is
- p-value approach
	- we know how strong evidence is