# Objective Metrics to Evaluate Residual-Echo Suppression During Double-Talk for the Stereophonic Case (Interspeech 2022).
### Amir Ivry, Prof. Israel Cohen, Dr. Baruch Berdugo <br/> 
#### Andrew and Erna Viterbi Faculty of Electrical and Computer Engineering, Technion - Israel Institute of Technology
> Speech quality, as evaluated by humans, is most accurately assessed by subjective human ratings. The objective acoustic echo cancellation mean opinion score (AECMOS) metric was recently introduced and achieved high accuracy in predicting human perception during double-talk. Residual-echo suppression (RES) systems, however, employ the signal-to-distortion ratio (SDR) metric to quantify speech-quality in double-talk. In this study, we focus on stereophonic acoustic echo cancellation, and show that the stereo SDR (SSDR) poorly correlates with subjective human ratings according to the AECMOS, since the SSDR is influenced by both distortion of desired speech and presence of residual-echo. We introduce a pair of objective metrics that distinctly assess the stereo desired-speech maintained level (SDSML) and stereo residual-echo suppression level (SRESL) during double-talk. By employing a tunable RES system based on deep learning and using 100 hours of real and simulated recordings, the SDSML and SRESL metrics show high correlation with the AECMOS across various setups. We also investigate into how the design parameter governs the SDSML-SRESL tradeoff, and harness this relation to allow optimal performance for frequently-changing user demands in practical cases. You are also encouraged to refer to the published [paper](https://www.researchgate.net/profile/Amir-Ivry/publication/361789204_Objective_Metrics_to_Evaluate_Residual-Echo_Suppression_During_Double-Talk_in_the_Stereophonic_Case/links/62c542b0db1d233df1cca7a1/Objective-Metrics-to-Evaluate-Residual-Echo-Suppression-During-Double-Talk-in-the-Stereophonic-Case.pdf).
> Demo can be found [_here_](https://soundcloud.com/ai4audio/sets/objective-metrics-to-evaluate-residual-echo-suppression-during-double-talk). 


## Table of Contents
* [General Info](#general-information)
* [Setup](#setup)
* [Usage](#usage)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)


## General Information
This repository highly relies on other repository of mine called "DSML-and-RESL-measures" that applies the DSML and RESL to the mono acoustic echo cancellation case. Therefore, this README is relatively brief to not repeat content, and more elaboration can be found on the mentioned repo. The attached code implements the two measures we developed to better assess speech quality and echo suppression during double-talk for the stereophonic acoustic echo cancellation case.

## Setup
To prepare for usage, the user should follow these steps:
- Clone this repo
- Set up a virtual environment and run: `pip install -r requirements.txt`
- Create a parent direcotry and assign its relative path to `data_path` variable inside `main.py`
- Inside this dir, locate each example in a separate subdirectory with a unique name. Every subfolder must contain, from each of the two stereophonic channels, the near end speech, the RES input before the system gain, and the RES prediction after the system gain, all in the time domain (.wav format). The names of these 6 (3 signals x 2 channels) files are user-dependent, but should not vary accross subdirectories. Assign the files names to `patterns` inside `main.py` and ensure the order of appearance is as given above.


## Usage
After setup, the user should follow these steps to use the code:
- run: `main.py`
- The log file `evaluation_metrics.txt` (the name is hard-coded) will appear inside the path assigned to the variable `data_path` (see _Setup_ for details). It contains the mean and standard deviation values of the DSML and RESL measures for every subdirectory.


## Acknowledgements
This research was supported by the Pazy Research Foundation, the Israel Science Foundation (ISF), and the International Speech Communication Association (ISCA). We would also like to thank stem audio for their technical support.<br/> If you use this repo or other instance of this research, please cite the following: <br/>
`@inproceedings{ivry2021objective,`<br/>
  `title={Objective Metrics to Evaluate Residual-Echo Suppression During Double-Talk in the Stereophonic Case},`<br/>
  `author={Ivry, Amir and Cohen, Israel and Berdugo, Baruch},`<br/>
  `booktitle={Interspeech},`<br/>
  `year={2022},`<br/>
`}`


## Contact
Created by [Amir Ivry](https://www.linkedin.com/in/amirivry/) - feel free to contact me also via [amirivry@gmail.com](amirivry@gmail.com).
