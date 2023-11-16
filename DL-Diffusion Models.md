[github repo containing papers](https://github.com/diff-usion/Awesome-Diffusion-Models)
[youtube video with coding](https://www.youtube.com/watch?v=a4Yfz2FxXiY)

## Theory
[youtube theory explaination](https://www.youtube.com/watch?v=HoKDTa5jHvg)
keywords
- variational lower bound
- sinusodial embedding
#### Steps
- Forward Process
	- adds noise by different methods, $q(x_t|x_{t-1})=N(output, mean, variance)$
	- $output=x_t$
	- $mean=\sqrt{1-\beta_t}x_t$
	- $variance=\beta_tI$
		- Linear noise scheduler
		- cosine noise scheduler
- Reverse Process
	- removes noise step by step, $p(x_{t-1}|x_t)$
		- uses U-net architechture

### Papers
- DDPM - 
	- Linear Noise Scheduler
		- redundant image at the end
### OpenAI paper
Cosine Noise Scheduler
- updates
	- increase depth, decrease width
	- more atention layers
	- increase attention heads
	- BigGAN residual block
	- Adaptive group normalization
	- Classifier Guidance

## Main components
- Noise Scheduler
- Neural Network (U-Net)
- Timestamp Encoding

## Implementations
- [youtube](https://www.youtube.com/watch?v=TBCRlnwJtZU)
- [stable diffusion](https://www.youtube.com/watch?v=ltLNYA3lWAQ)
