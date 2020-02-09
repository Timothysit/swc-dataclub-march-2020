---
title: Multisensory sensory integration in the mouse cortex
separator: <!--h-->
verticalSeparator: <!--v-->
theme: white
revealOptions:
    transition: 'fade'
---


# Multisensory sensory integration in the mouse cortex

## AKA what I plan to do during my PhD

### 2020 February 24 

<!--h-->



## What is multisensory integration?

<!--h-->


## Where does multisensory integration occur? 

<!--h-->

 - include graphic here showing 
    - ease of recording (x-axis) 
	- probability of getting multisensory response 
	- expected number of neuorns that can be recorded from simultaneously (either 2P or neuropixels)

## Is multisensory activity linear or linear? 

<!--h-->


## What determines whether multisensory activity will occur/develop? 

 - temporal coherence 
 - is supervised learning required for multisesnory integration in the cortex? 


<!--h-->


## Filmworld: passive presentation of video with natural scene statistics

 - what is natural scene statistics and why is it important? 
    - high dimensional
	- (ecologically relevant?)
 - include figure of the design of filmworld 
 
## Filmworld for addresssing the linearity question 

## Filmworld for addressing the how question of multisensory integration 

 - present set of stimulus multiple times 
 - some of them temporally coherent and 'true' (occurs in nature)
 - some of them temporally incoherent and 'true' (animal and some background sound) 
 - some of them temporally coherent but false (artificial sounds, dubbing) 
 - some of them temporally inchoerent and false (random video and random audio)


## Multispaceworld 


# Results 

## Filmworld 

### Recording regions / (experiments performed so far)

### Summary of neural response

## Multispaceworld 

### Summary of neural response 

 - how many are unimodal 
 - how many are audiovisual 




# Future directions 







### dPCA: input data format

<div id='left'>

![Condition-decision matrix](./notebook/condition_decision_matrix.png) <!-- .element height="60%" width="90%"; -->

</div>

<div id='right'>

![Data matrix input for dPCA](./notebook/data_matrix.png) <!-- .element height="60%" width="90%"; -->

</div>

<font size=5>
where you have $N$ neurons, $K$ trials, $S$ stimulus, $D$ decisions and $T$ time points
</font>

<!--v-->
 
### dPCA: taking the mean 

![Taking the mean across a dimension dPCA matrix](./notebook/matrices_tiled_in_3D.png) <!-- .element height="70%" width="70%"; -->

<!--v--> 
 
### dPCA: objective 

<font size=6>
We only want to reconstruct the contribution of each experimental variable individually.

Remember: the $X_\phi$ matrices are those averages, plus some residual contribution/noise
</font>

$$
X = \sum_{\phi = ( t, ts, td, tsd )} X_\phi + X_\text{res}
$$

<!--v-->

### dPCA: objective 

<font size=6>

This can be done by having a separate decoder transformation matrix (PCA: same matrix to compress and map back to the original space):

</font>

$$
\mathcal{L}_\text{dPCA}^\phi = \vert\vert \mathbf{X}_\phi - \mathbf{F}_\phi\mathbf{D}_\phi\mathbf{X} \vert\vert^2
$$

<font size=5>

where: 

 - $\mathbf{D}_\phi$ is used to compress the data into a space with fewer dimensions 
 - $\mathbf{F}_\phi$ is used to map the data to the mean activity of interest (PCA: original data) 

</font>

<!--v-->

Demixed PCA tries to balance two goals: demixing and summarising .

![Demixed PCA example](./figures/dPCA/fig-2-bdf.png) 

<!--h-->




<div id='left'>
 
![Component and variance](./figures/dPCA/fig-3-cd.png) <!-- .element height="70%" width="70%";  -->

</div>

<div id='right'>

<font size=4>

1. Stimulus component: axis that best demixes the differences in neural activity due to differences in stimulus 
2. Decision component: differences in decision (and time) best demixes
3. Interaction component: variability due to interaction between stimulus and decision 
4. Condition-independent: does not depend on  particular stimulus / decision, but due to either factors that vary with time (eg. the fact that you are presenting the vibration from time $t_1$ to time $t_2$)
 
</font>
 
 </div> 


<!--v-->

### Example of applying demixed PCA: looking at how each PC vary with time 

![Changes of projected neural activity over time](./figures/dPCA/fig-3-b.png) <!-- .element height="50%" width="50%"; style="margin:auto;display:block" -->

<!--h--> 

### Caveats of dPCA

<font size=6>

It does not work if: 

 - you don't have all combinations of task parameters 
 - continuous task parameters 
 - you need a lot more neurons than your task parameters 
 
 
 There are workarounds for: 
 
  - your trials are unbalanced (re-balancing procedure)
  - different trial lengths (time warping)
</font> 

<!--h-->

## Other demixing / summarising methods

<!--v-->


### Non-linear extension of dPCA using kernels (kdPCA)
[Latimer 2019: Nonlinear demixed component analysis for neural population data as a low-rank kernel regression problem](https://nbdt.scholasticahq.com/article/11523-nonlinear-demixed-component-analysis-for-neural-population-data-as-a-low-rank-kernel-regression-problem)

<!--v-->

#### Why do we need nonlinear methods? 


![Latimer kernel PCA demo](./figures/dPCA/latimer2018-fig-2ab.png) <!-- .element height="70%" width="60%"; style="margin:auto;display:block" -->



<!--v-->

<div id='left'>

Pros

 - it's non-linear: more flexibility 
 - (uses kernels)

</div>

<div id ='right'>

Cons 

 - extracted components are maybe less interpretable  
 - more parameter tuning (and so need more robust cross-validation)

</div>



<!--v-->

### Tensor Component Analysis (TCA)
[Williams et al. 2018: Unsupervised Discovery of Demixed, Low-Dimensional Neural Dynamcis across Multiple Timescales through Tensor Component Analysis](https://www.sciencedirect.com/science/article/pii/S0896627318303878)

<!--v-->


### What is tensor component analysis?

<div id='left'>

![Latimer kernel PCA demo](./figures/other-dim-reduce-methods/TCA-paper-figure-1.png) <!-- .element style="margin:auto;display:block" -->

</div>


<div id='right'>

<font size=5>

- a matrix is a second order tensor, and (d)PCA is a dimensionality reduction on second order tensors 
- TCA is a dimensionality reduction method on third order tensors 
- previous approaches to dimensionality reduction focus on two modes (tensor jargon for "axes"): neuron and time
- TCA is a way to add more modes to reduce dimensionality: eg. trials

</font>

</div>


<!--v-->


<div id='left'>

Pros

 - They claim it's a "natural generalization of PCA to higher-order tensors" 
 - unsupservised method 
 - can handle continuous experimental parameters

</div>

<div id ='right'>

Cons 

 - (Lucas thinks they are lying somewhere)
 - linear 
 - not dynamical
 - Joana and Maneesh have a different tensor method 
 
</div>

<!--v-->

### Latent Factor Analysis via Dynamical Systems (LFADS)

[Pandarinath 2018: Inferring single-trial neural population dynamics using sequential auto-encoders](https://www.nature.com/articles/s41592-018-0109-9)


<!--v-->

<div id='left'>

Pros

 - dynamical model: you enforce temporal correlation (you don't assume time points are independent)
 - (it is more true)


</div>

<div id ='right'>

Cons 

 - does not demix; only summarise 
 - do we like RNNs?
 
 
</div>


<!--h-->


### Other methods we have no time to talk about 

 - Gaussian Process Factor Analysis 
 - Independent Component Analysis
 - tSNE
 
 
 Good reviews papers:

 - [Cunningham and Byron 2014: Dimensionality reduction for large-scale neural recordings](https://www.nature.com/articles/nn.3776)
 
<!--v-->

#### tSNE 

<iframe frameborder="0" width="100%" height="500pt" src="https://distill.pub/2016/misread-tsne/"></iframe>


<!--h-->

### Comparing dimensionality reduction methods


![Dim reduction methods comparison](./notebook/dim_reduction_methods_prop.png) <!-- .element height="70%" width="60%"; style="margin:auto;display:block" -->





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

p { text-align: left; }

#myfigure{
	text-align: center;
}
</style>


