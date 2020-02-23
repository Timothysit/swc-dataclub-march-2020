---
title: Multisensory sensory integration in the mouse cortex
separator: <!--h-->
verticalSeparator: <!--v-->
theme: white
revealOptions:
    transition: 'fade'
---


<style>
.reveal section img { background:none; border:none; box-shadow:none; }
.reveal h1 { font-size: 2em; }
.reveal h2 { font-size: 1em; }
</style>



<font size=5>

# Audio-visual integration in the mouse cortex

</font>

<font size=5>

## AKA what I plan to do during my PhD

</font>

<font size=5>

### Tim Sit

</font>

<font size=3>

### 2020 February 24 

</font>

<!--h-->



## Outline 

 1. General thoughts about studying audio-visual intgeration
 2. Passive audio-visual response: experiment design and some preliminary analysis 
 3. Audio-visual decision making: electrophysiology analysis from Pip's data
 



<!--h-->

<font size=5>

## What is a multimodal neuron?

</font>

*Neuron respond to presense / specific property of more than one sensory modality.*

<div id='left'>

![Visual response neuron](./figures/visual_response_identity.png) 

</div>

<div id='right'>

![Audio response neuron](./figures/audio_response_presense.png) 

</div>

<!--h-->

<font size=5>

## Where does multimodal integration occur? 

</font>


![Where to find multimodal response](./figures/where_to_find_multimodal_response.png) 

	
 <!--h-->

<font size=5>

## What is the relationship between multimodal response and unimodal response?

</font>

<div id='left'>

![Linear multimodal response](./figures/linear_multimodal_response.png) 

$$
f(A + V) = f(A) + f(V)
$$

</div>

<div id='right'>

![Nonlinear multimodal response](./figures/nonlinear_multimodal_response.png) 

$$
f(A + V) = f(A) + f(V) + f(A, V)
$$

</div>

<!--h-->

### What are the neural mechanisms of multimodal decision making?

![Race model intergation model](./figures/decision-models/late-integration-2.png)

![Drift model integraation model](./figures/decision-models/late-integration-1.png)

<!--v-->

![Early integration model](./figures/decision-models/early-integration.png)


<!--h-->

### Two main experiments to tackle the above questions 

<div id='left'>

Passive video presentation


<video controls width="500">
	   <source src="./videos/seal.webm" type="video/webm">
	    <source src="./videos/seal.mp4" type="video/mp4" >
</video>


</div>


<div id='right'>

Audio-visual decision making task 

![Pip's multispaceworld task](./figures/pip-multispaceworld-task-outline.png)


</div>



<!--v-->


## What determines whether multisensory activity will occur/develop? 

 - temporal coherence?
 - is supervised learning required for multimodal integration in the cortex? 
     - eg. associating reward / punishment to specific audio-visual pair 
	 - eg. decision making task


<!--h-->


## Filmworld: passive presentation of video with natural scene statistics

![Filmworld combinations](./figures/filmworld_all_combinations_manual_cropped.png) 


<!--v-->



<img src="./figures/filmworld_all_videos.png" alt="Girl in a jacket" width="700" height="600">



<!--v-->

Overall session structure 

![Filmworld session structure](./figures/filmworld_experiment_overview_structure.png)


Individual trial structure

![Filmworld trial structure](./figures/filmworld_trial_structure.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->

 <!--v-->
 
Three presentation methods being tested 

<font size=4>

Gray interval (4 seconds / video)

</font>

![Interval method](./figures/filmworld/example-frames-int.png)

<font size=4>

Continuous (6 seconds / video)

</font>

![Continuous method](./figures/filmworld/example-frames.png)

<font size=4>

Fading (6 seconds / video)

</font>

![Fading method](./figures/filmworld/example-frames-fade.png)
 

 
 <!--v-->
 
 
 Why natural videos > gratings / pure tones:
  
   - high dimensional
	  - look at high dimensional neural activity 
	  - more likely to evoke audio-visual activity
   - (ecologically relevant?)
 
  <!--v-->
  
<!--h-->

## Filmworld: example activity from one experiment

![Example activity (colorbar should be deconvovled rate I think)](./figures/filmworld/2p/TS003/2019-11-28/exp-2/test-audio-video-pair-all-cell.png)

 <!--v-->
 
### Mean activity of a neuron to each audio-video pair 

![Example visual neuron mean activity](./figures/filmworld/2p/TS003/2019-11-28/exp-2/test-audio-video-pair-cell-74.png)

 <!--v-->


### Recording from 12 planes 

![Mean image of the 12 planes](./figures/filmworld/2p/TS003/2019-11-28/exp-2/all-planes-plot.png)

The first plane is always removed from analysis.

 <!--v-->
 
### There is more activity when a movie is playing 

<div id='left'>

![Single neuron activity throughout experiment](./figures/filmworld/2p/TS003/2019-11-28/exp-2/single_neuron_trace_plane_number_7neuron_15.png)

</div>



<div id='right'>

![Movie vs. no movie unity plot](./figures/filmworld/2p/TS003/2019-11-28/exp-2/movie_vs_no_movie_mean_activity.png)

</div>


<!--h-->

## Does PPC/V1 contain information about video and/or audio stimulus?

Population decoding approach

![TS003 audio/video decoding SVM](./figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/simple-svm-cv-split-classfication-accuracy.png) <!-- .element  width="40%"; style="margin:auto;display:block" -->

<!--v-->

<font size=5>
  
### Decoding using different classifiers 

</font>


<div id='left'>


![TS003 video decoding diff classifiers](./figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/video-decoding-performance-diff-classifiers.png)


</div>


<div id='right'>

![TS003 audio decoding diff classifiers](./figures/filmworld/2p/TS003/2019-11-28/exp-2/av-classification/audio-decoding-performance-diff-classifiers.png)

</div>


<!--v-->

<font size=5>

### Another example 

</font>

<div id='left'> 

![TS004 audio / video decoding](./figures/filmworld/decoding/TS004-2019-12-18-1-PC-SVM-classification-accuracy.svg)

</div>


<div id='right'>

![TS004 audio / video decoding](./figures/filmworld/decoding/TS004-2019-12-18-1-PC-KNN-classification-accuracy.svg)

</div>

<!--v-->

### Other ideas

 - look at one-to-one decoding 
 - tune reguarlisation parameter
 


<!--h-->

## Looking at audio / visual response in individual neurons 

<font size=5>

by looking at correlation across repeats

</font>

![TS004 interval video neuron](./figures/filmworld/correlation/old_figs/plane_7_cell_45audio_0_correlation.png)


<!--v-->

![TS004 interval another example](./figures/filmworld/correlation/TS004_interval_plane_5_cell_497audio_0_correlation.png)




<!--h-->

<font size=5>

some neurons seem to care about auditory stimulus

</font>

![TS004 interval audio neuron](./figures/filmworld/correlation/old_figs/plane_1_cell_31video_0_correlation.png)

<!--v-->


![TS004 audio neuron another example](./figures/filmworld/correlation/TS004_interval_plane_2_cell_33video_0_correlation.png)


<!--h-->

<font size=5>

## Are neurons more correlated in video-only conditions than audio-only conditions?

</font>

![Correlation scenaruios](./figures/correlation_conceptual_figure_4_conditions.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->


<!--h-->



<font size=5>

## Are neurons more correlated in video-only conditions than audio-only conditions?

</font>


![TS004 interval all neuron audio and video corr](./figures/filmworld/correlation/TS004_interval_experiment_all_neuron_correlation.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->

<!--v-->

![TS004 continuous experiment](./figures/filmworld/correlation/TS004_continuous_experiment_all_neuron_correlation.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->

<!--h-->


![TS004 interval audio-video neuron video respones](./figures/filmworld/correlation/old_figs/plane_5_cell_342audio_0_correlation.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->


![TS004 interval audio-video neuron audio respones](./figures/filmworld/correlation/old_figs/plane_5_cell_342video_0_correlation.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->



<!--h-->


### Future directions

1. Improve recording of timing of stimulus onset (esp. auditory stimulus)
2. Correlate neural activity with audio energy, video energy, and body movement
3. Auditory cortex recording

<!--h-->
 


## Multispaceworld: neural basis of multisensory decision making

![Race model intergation model](./figures/decision-models/late-integration-2.png)

![Drift model integraation model](./figures/decision-models/late-integration-1.png)

<!--v-->

<div id='left'>

Race model

![Race model](./figures/decision-models/race_model.png)

</div>

<div id='right'>

Drift model

![Drift model](./figures/decision-models/drift_model.png)


![Coherent vs. conflict reaction time](./figures/pip_data_coherent_conflict_rt.png) <!-- .element  width="50%"; style="margin:auto;display:block" --> 



</div>



<!--v-->




<!--h-->

## MOs contains information about choice 


and as demonstrated by optogenetic inactivation, is necessary for multisensory decision making


<div id='left'>

![Movement aligned movement decoding bar chart](./figures/multispaceworld/decode_left_right_100ms_before_movement_brain_region_accuracy_bar_chart.svg)

</div>

<div id='right'>

![Stimulus aligned movement decoding bar chart ](./figures/multispaceworld/decode_left_right_100ms_after_stimulus_brain_region_accuracy_bar_chart.svg)

</div>

<!--v-->

<div id='left'>

Aligned to stimulus

![Stimulus aligned movement decoding](./figures/multispaceworld/decode_response_lr_stim_aligned_all_subject_exp_averaged_rel_accuracy_.svg)

</div> 

<div id='right'>

Aligned to movement

![Movement aligned movement decoding](./figures/multispaceworld/all_subject_exp_averaged_rel_accuracy_decode_lr_aligned_to_movement.svg)

</div>


<!--v-->

<div id='left'>

![Coherent vs. conflict condition movement decoding](./figures/multispaceworld/decode_left_right_100ms_before_movement_coherent_conflict_accuracy_bar_chart.svg)

</div>

<div id='right'>

![Auditory vs. visual trials movement decoding](./figures/multispaceworld/decode_left_right_100ms_before_movement_aud_vid_only_accuracy_paired_scatter_chart.svg)

</div>


<!--v-->

<font size=5>

Choice information comes early

</font>

<img src="./figures/multispaceworld/active-psth/early_movement_no_passive_response_s3_e21_b2_sig_idx_10_combined_exp_cell_idx_95.png" alt="Active and passive responsive neuron" width="700" height="600">



<!--v-->

<font size=5>

Some MOs respond in both active and passive condition

</font>

<img src="./figures/multispaceworld/active-psth/early_movement_decoding_subject_2_brain_area_3_exp_15_sig_idx_2_combined_exp_cell_idx_23.png" alt="Active and passive responsive neuron" width="700" height="600">



<!--v-->


<font size=5>

Some are just related to movement

</font>


<img src="./figures/multispaceworld/active-psth/after_movement_left_right_s3_e21_b2_sig_idx_16_combined_exp_cell_idx_82.png" alt="Active and passive responsive neuron" width="700" height="600">








<!--h-->



## MOs may not be purely motor 

Passive direction-dependent auditory response in MOs 

<div id='left'>

![Stimulus time aligned auditory response](./figures/multispaceworld/passiveReponse/aud_left_right_subject_4_exp_32_cell_48.png) <!-- .element  width="100%"; style="margin:auto;display:block" -->

</div>


<div id='right'>

![Stimulus time aligned auditory response scatter ](./figures/multispaceworld/passiveReponse/aud_left_right_subject_4_exp_32_cell_48_scatter.png) <!-- .element  width="100%"; style="margin:auto;display:block" -->

</div>


<!--v-->

<font size=5>

### Decoding of auditory direction in passive condition is poor using all neurons

</font>

<font size=5>

Decoding audio left/right in the same experiment as the example cell shown before 

</font>

![Audio left/right decoding](./figures/multispaceworld/passiveReponse/subject_4_exp_32__left_right_windowed_classification_svm_l1_C_untuned_w_hline_w_error_shade_brain_regions_combined.png) <!-- .element  width="60%"; style="margin:auto;display:block" -->

<!--v-->


### MOs responds to audio onset in passive conditions 

<div id='left'>

![Audio on/off activated](./figures/multispaceworld/passiveReponse/aud_on_off_subject_3_exp_21_cell_89_scatter.png)

</div>

<div id='right'>

![Audio on/off suppressed](./figures/multispaceworld/passiveReponse/aud_on_off_subject_4_exp_34_cell_34_scatter.png)


</div>


<!--v-->


### Time of auditory and visual information 

<font size=5>

Observation: 

 - auditory response is faster than visual response 
 - auditory response show an early peak and late peak in activity

Hypothesis: 

 - early peak in auditory response may signal auditory presense 
 - whereas late auditory activity may signal auditory direction 
 - this may explain auditory dominance effect observed in go/no-go task 
 
 
 </font>
 
 <!--v-->
 
 ![Example neuoron that is close to illustrating the point](./figures/multispaceworld/peri_stimulus_audio_left_right_subject_6_experiment_54_cell_70w_grid_unimodal_only.svg)
  

<!--v-->


![Mean of peak time ](./figures/multispaceworld/timeOfInfo/all_exp_sig_neuron_mean_time_of_peak_neuron_type_grouped_threshold_0p05.svg)

 
 <!--h-->
 

# Future directions 

<font size=7>
 
1. More analysis of time course of audio and visual information 
2. Relate auditory/visual bias in behaviour with neural activity
3. Summarise main neuron types in MOs
 
 
 </font>
 

 <!--h-->
 
# Thanks to 


 - Pip: ephys analysis, rigbox help and rich tea biscuits
 - St&eacute;phane, Sam, Lauren, Michael: 2P 
 - Charu: surgery and animals
 - Bex: animals
 - Anwar, Kush, Sam, C&eacute;lian: analysis discussions 
 - Jai and Miles: setting up video playback in rigbox-signals

 <!--v-->
 
## Technical acknowledgments 

 - running experiments: rigbox, signals
 - 2P data processing: suite2p, facemap 
 - Data organisation: xarray, dask, pandas
 



 <!--h-->


## Other ideas

<!--v-->

## Filmworld for addressing the how question of multisensory integration 

 - present set of stimulus multiple times 
 - some of them temporally coherent and 'true' (occurs in nature)
 - some of them temporally incoherent and 'true' (animal and some background sound) 
 - some of them temporally coherent but false (artificial sounds, dubbing) 
 - some of them temporally inchoerent and false (random video and random audio)







 




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


