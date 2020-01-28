---
title: dPCA 
separator: <!--s-->
verticalSeparator: <!--v-->
theme: white
revealOptions:
    transition: 'fade'
---




# demixed Principal Component Analysis

[Kobak et al 2016: Demixed principal component analysis of neural population vector](https://elifesciences.org/articles/10989)


<!--s-->

## What is 'demixing'? 

  - Goal of demixing: you want to find patterns of activity that best separate out experiment conditions
  - 'Experiment conditions' includes stimulus and animal response
  
## Single-neuron versus population level demixing 

 - The 'standard' approach of neuroscience: performing a t-test (or any two-sample comparison test) of the firing rate of each neuron before and after the stimulus/response can be thought of as demixing. 
  - you find $x$ % of neurons that respond to $a$ and $y$ % of neurons that respond to $b$
  - however, you limit the space of neural activity which you think provides information about the stimulus; you only consider 
  - a better approach will be to consider the activity of all neurons together: do demixing at the population level 
  
  

## Approaches to demixing 




## Principles of dimensionality reduction for demixing 


<!--s-->


## demixed PCA

### What is the objective of demixed PCA?

demixed PCA tries to balance two goals: demixing and compression.

![Demixed PCA example](https://github.com/timothysit/dPCA-journal-club/figures/dPCA/fig-2-bdf.png)

<!--s-->

### Example of applying demixed PCA : task

Romo 1999: Monkeys compare frequency of two vibrations 

![Romo 1999 task](https://github.com/timothysit/dPCA-journal-club/figures/dPCA/romo-1999-fig-1ab.png)

<!--s-->

### Example of applying demixed PCA : input data

 - Input data: we separate out our neural data based on stimulus condition: there are 12 possible stimulus conditions 
 - The input data is also separated out according to 2 decisions 
 - You then run dPCA through this data 
 
 <!--s-->
 
### Example of applying demixed PCA : output of dPCA 

Same as PCA, dPCA gives you the top $n$ (user-specified) principal components. 
But dPCA also gives you the experimental variable which the component explains most of the variability of neural activity: 

 1. Stimulus component: differences in stimulus best demixes this 'pattern' (dimension) of neural activity 
 2. Decision component: differences in decision best demixes
 3. Interaction component: variability due to interaction between stimulus and decision 
 4. Condition-independent: does not depend on particular stimulus / decision, but due to either factors that vary with time (eg. the fact that you are presenting the vibration from time $t_1$ to time $t_2$
 
![Component and variance](https://github.com/timothysit/dPCA-journal-club/figures/dPCA/fig-3-cd.png)

<!--s-->

### Example of applying demixed PCA: looking at how each PC vary with time 

![Changes of projected neural activity over time](https://github.com/timothysit/dPCA-journal-club/figures/dPCA/fig-3-b.png)


<!--s-->

### Code


<!--s-->

## Other dimensionality reduction methods 

Good reviews papers:

 - [Cunningham and Byron 2014: Dimensionality reduction for large-scale neural recordings](https://www.nature.com/articles/nn.3776)
 


<!--s-->

### PCA 

<!--s-->


### Factor analysis

<!--s-->



### t-SNE

<iframe frameborder="0" width="100%" height="500pt" src="https://distill.pub/2016/misread-tsne/"></iframe>

<!--v-->

<div id='left'>

Pros

 - list 
 - of 
 - pros

</div>

<div id ='right'>

Cons 

 - list 
 - of 
 - cons

</div>

<!--v-->

Some example implementations:

 - [Dimitriadis 2018: t-SNE visualization of large scale neural recordings](https://www.mitpressjournals.org/doi/full/10.1162/neco_a_01097)



<!--s-->


### Gaussian Process Factor Analysis 

<!--s-->

### Independent Component Analysis 

<!--s-->

### Latent Factor Analysis via Dynamical Systems (LFADS)



[Pandarinath 2018: Inferring single-trial neural population dynamics using sequential auto-encoders](https://www.nature.com/articles/s41592-018-0109-9)



<!--s-->


### Tier-list of dimensionality reduction methods










<style>

#left {
	margin: 10px 0 15px 20px;
	text-align: left;
	float: left;
	z-index:-10;
	width:48%;
	font-size: 0.85em;
	line-height: 1.5; 
}

#right {
	margin: 10px 0 15px 0;
	float: right;
	text-align: left;
	z-index:-10;
	width:48%;
	font-size: 0.85em;
	line-height: 1.5; 
}

</style>


