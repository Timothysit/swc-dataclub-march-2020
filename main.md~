---
title: From 2020-01-08 to 2020-01-17
separator: <!--s-->
verticalSeparator: <!--v-->
theme: white
revealOptions:
    transition: 'fade'
---




# Progress update 2020 Jan 8 - 2020 Jan 17

<!--s-->

## B2 Rig Upgrade

Stimulus computer: 

 - DDR4 RAM 
 - 


<!--s-->

# 2P Analysis

<!--s-->


## 2P analysis: finding neurons that respond to audio 

TS003-plane-7-cell-24


![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/audio-marignal-response-bar-chart/audio_marginal_reponse_cell_24.png) <!-- .element height="70%" width="100%"; -->

<!--s-->

### TS003-plane-7-cell-24

![image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/test-audio-video-pair-cell-24.png) <!-- .element height="70%" width="100%"; -->


<!--s-->

## 2P analysis: Decoding video and audio

Simple SVM classifier with default parameters.
Using about 400 cells from one plane.

![image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/simple-svm-cv-split-classfication-accuracy.png) <!-- .element height="50%" width="50%"; -->

<!--s-->

### Video decoding

![image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/video-decoding-performance-diff-classifiers.png)

<!--s-->

### Audio decoding

![image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/audio-decoding-performance-diff-classifiers.png)


<!--s-->

### Using all cells 

Caveat: some planes weren't manually curated yet, so may be noisy.

![image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/knn-classifier-w-diff-PCs-subject-TS003-exp-2.png) <!-- .element height="50%" width="80%"; -->



<!--s-->


# Ephys Analysis 

<!--s-->

## Classifying cells 

<iframe width="100%" height="600pt" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTk1w56bgGRBI4aoc4njVzvys9-WC60yz7livo-JODzwurYubD0fk5pxAZ6lnBqduOSZeu2rrOMwB4P/pubhtml?widget=true&amp; headers=false";></iframe>

<!--s-->

## Main cell types 

 1. Go sustained firing 
	 - eg. subject-2-brain-loc-2-cell-20
 2. No-go enhanced cells
    - eg. subject-2-brain-loc-3-cell-5
	- a lot also seems to respond to audio in passive condition 
 3. Trial-onset neurons 
 4. Movement / choice-related neurons that also respond to audio in passive condition 
 5. Trial/audio onset suppressed cells 
    - suppressed: subject-3-brain-loc-1-cell-48
	- enhanced w/ sharp peak: subject-3-brain-loc-1-cell-53
 
 <!--s-->

 

## Some rare but intesting cell types

 <!--s-->

### 1. Audio-visual interaction 

eg. subject-2-brain-loc-2-cell-80
 ![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/combined-alignment-subsubset-m-300p750bin80/subject-2/brain-area-3/exp-15/sig_idx_4_combined_exp_cell_idx_1.png) <!-- .element height="70%" width="70%"; margin-left="auto"; margin-right="auto" -->
 
 <!--v-->
 
subject-2-brain-loc-3-cell-1


 
 <!--s-->
 
### 2. Audio neurons with no movement response
  
subject-3-brain-loc-2-cell-21

![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/combined-alignment-subsubset-m-300p750bin80/subject-3/exp-21/brain-area-2/exp-21/sig_idx_58_combined_exp_cell_idx_21.png) <!-- .element height="70%" width="70%"; margin-left="auto"; margin-right="auto" -->




<!--s-->

## $f(a_{l}v_l) = f(a_l) + f(v_l)?$

<iframe frameborder="0" width="700pt" height="700pt" src="https://timothysit.github.io/cortex-lab-weekly-reports/figures/multispaceworld-ephys/linked_selection_subsets_stretch.html"></iframe>

<!--s-->

## Cell 89

![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/combined-alignment-subsubset-m-300p750bin80/subject-3/exp-21/brain-area-2/exp-21/sig_idx_3_combined_exp_cell_idx_89.png) <!-- .element height="70%" width="70%"; -->



<!--s-->

## First attempt at neural trajectories 

### Without PCA 




<!--s-->

### With PCA 

![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/multispaceworld-ephys/pop-analysis/mean_left_right_grid_trajectory_PCA_20.png) <!-- .element height="70%" width="70%"; -->


<!--s-->

### With PCA + Whitening 

![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/multispaceworld-ephys/pop-analysis/mean_left_right_grid_trajectory_PCA_20_whiten.png) <!-- .element height="70%" width="70%"; -->

<!--s-->

### Explained variance 

<div id="left"> 

#### Left choice

![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/multispaceworld-ephys/pop-analysis/left_movement_matrix_PCA_explained_variance.png) <!-- .element height="70%" width="100%"; -->

</div> 


<div id="right"> 

#### Right choice


![Image](https://timothysit.github.io/cortex-lab-weekly-reports/figures/multispaceworld-ephys/pop-analysis/right_movement_matrix_PCA_explained_variance.png) <!-- .element height="70%" width="100%"; -->

</div> 









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


