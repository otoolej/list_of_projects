# :sparkles: Directory of Projects
## Algorithms for Neonatal EEG (+ NIRS), Signal Processing Tools, Machine Learning Methods, and More


Directory of repositories on this [Github page](https://github.com/otoolej/). :octocat:

Computer code for analysing neurophysiological signals :brain:, including EEG and NIRS,
recorded from infants in the neonatal intensive care unit. :baby: :hospital: 

Also includes code for generic signal processing tools (such as time--frequency analysis)
and machine learning tools.

___

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [Quantitative EEG (qEEG)](#quantitative-eeg-qeeg)
    - [NEURAL -- a neonatal EEG feature set in Matlab (and Python)](#neural----a-neonatal-eeg-feature-set-in-matlab-and-python)
- [Detecting Bursts or Inter-Bursts in Neonatal EEG](#detecting-bursts-or-inter-bursts-in-neonatal-eeg)
    - [Inter-Burst Detector](#inter-burst-detector)
        - [Preterm EEG](#preterm-eeg)
            - [Method: features + SVM](#method-features--svm)
            - [Method: single feature](#method-single-feature)
        - [Term EEG (in trace alternant activity)](#term-eeg-in-trace-alternant-activity)
    - [Burst Detector](#burst-detector)
        - [Preterm EEG](#preterm-eeg-1)
- [Near Infraread Spectroscopy (NIRS)](#near-infraread-spectroscopy-nirs)
    - [Synthetic NIRS signals](#synthetic-nirs-signals)
    - [Method to extract transient components from NIRS signal](#method-to-extract-transient-components-from-nirs-signal)
- [Heart Rate Variability (HRV)](#heart-rate-variability-hrv)
    - [Standard features of HRV](#standard-features-of-hrv)
- [Tools for Time--Frequency Signal Analysis](#tools-for-time--frequency-signal-analysis)
    - [Fast and Memory Efficient Algorithms for Computing Time--Frequency Distributions (TFD)](#fast-and-memory-efficient-algorithms-for-computing-time--frequency-distributions-tfd)
    - [Methods to Estimate the Instantaneous Frequency from TFDs](#methods-to-estimate-the-instantaneous-frequency-from-tfds)
- [Tools for Connectivity](#tools-for-connectivity)
    - [Features of Nonstationary Directional Coupling](#features-of-nonstationary-directional-coupling)
- [Signal-Processing and Machine-learning Tools](#signal-processing-and-machine-learning-tools)
    - [Random Convolution Kernels with Multiscale Decomposition](#random-convolution-kernels-with-multiscale-decomposition)
    - [Mutual information estimates](#mutual-information-estimates)
    - [Envelope--Derivative Operator](#envelope--derivative-operator)
- [Code to Accompany Published Papers](#code-to-accompany-published-papers)
    - [Plots for Review Paper on Time--Frequency Processing of Nonstationary Biomedical signals](#plots-for-review-paper-on-time--frequency-processing-of-nonstationary-biomedical-signals)
    - [Monitoring cerebral oxygenation of preterm infants using a neonatal specific sensor](#monitoring-cerebral-oxygenation-of-preterm-infants-using-a-neonatal-specific-sensor)
    - [Quantitative features of the EEG recorded minutes after birth](#quantitative-features-of-the-eeg-recorded-minutes-after-birth)
    - [Evolution of qEEG in preterm infants over the first days of life](#evolution-of-qeeg-in-preterm-infants-over-the-first-days-of-life)
    - [EEG concordance in preterm twins](#eeg-concordance-in-preterm-twins)

<!-- markdown-toc end -->

___

# Quantitative EEG (qEEG)
## NEURAL -- a neonatal EEG feature set in Matlab (and Python)
- Curated set of quantitative features for neonatal EEG.
- Clearly defined features (full description and accompanying code).
- code: [github (Matlab version)](https://github.com/otoolej/qEEG_feature_set)
- code: [github @BrianMur92 (Python version)](https://github.com/BrianMur92/NEURAL_py_EEG_feature_set)
- paper (preprint): [arXiv:1704.05694](https://arxiv.org/abs/1704.05694)

___

# Detecting Bursts or Inter-Bursts in Neonatal EEG

## Inter-Burst Detector 
### Preterm EEG 
#### Method: features + SVM
- Machine learning method to detect inter-burst intervals in preterm EEG.
- Developed and tested on a cohort of infants <30 weeks gestational age.
- code: [github | Python version](https://github.com/otoolej/py_burst_detector)
- code: [github | Matlab version](https://github.com/otoolej/burst_detector)
- paper: [O'Toole et al., Med Eng Phys, 2017](https://doi.org/10.1016/j.medengphy.2017.04.003)

#### Method: single feature 
- Generic method to detect bursts: high-amplitude coupled with high-frequency.
- Includes envelope derivative operator (EDO) and nonlinear energy operator (NLEO).
- code: [github | Matlab version](https://github.com/otoolej/nonlinear-energy-operators)
- code: [github | Python version](https://github.com/otoolej/envelope_derivative_operator)
- paper: [O'Toole et al., EMBC-2014](https://doi.org/10.1109/EMBC.2014.6944325)


### Term EEG (in trace alternant activity)
- Machine learning method to detect bursts and inter-bursts in term EEG during Quiet Sleep.
- Trained and tested on a cohort of healthy, normal newborns.
- code: [github @sumitraurale | Matlab code](https://github.com/sumitraurale/interburst_detector)
- paper: [Raurale et al., EMBC-2020](https://doi.org/10.1109/EMBC44109.2020.9176147)


## Burst Detector 
### Preterm EEG
- Method to detect short-duration bursts of activity in preterm (<30 weeks GA) EEG.
- code: [github @BrianMur92 | Python code](https://github.com/BrianMur92/Preterm_transient_burst_detector)
- paper: [Murphy et al., EMBC-2020](https://doi.org/10.1109/EMBC44109.2020.9175154)

___

# Near Infraread Spectroscopy (NIRS)
## Synthetic NIRS signals
- Generates cerebral oxygenation-like signals (rcSO2).
- code: [github | Matlab code](https://github.com/otoolej/synth_NIRS_signals)
- papers: [O'Toole et al., EMBC-2018](https://doi.org/10.1109/EMBC.2018.8513523) and
 [Ashoori et al., EMBC-2021](https://doi.org/10.1109/EMBC46164.2021.9630560)

## Method to extract transient components from NIRS signal
- Method to extract sparse, transient-like signals from the cerebral oxygenation signals.
- Method is based on singular spectral analysis and signal rotation using the cosine transform.
- code: [github | Matlab code](https://github.com/otoolej/transient_decomp_ssa)
- paper: [Ashoori et al., EMBC-2021](https://doi.org/10.1109/EMBC46164.2021.9630560)

# Heart Rate Variability (HRV)
## Standard features of HRV
- Generates some standard features (e.g. spectral power ratios) of HRV.
- code: [github | Matlab code](https://github.com/otoolej/hrv_features_neonates)
- papers (e.g.): [Garvey et al., Pediatric Research, 2021](https://doi.org/10.1038/s41390-021-01412-x)

___

# Tools for Time--Frequency Signal Analysis

## Fast and Memory Efficient Algorithms for Computing Time--Frequency Distributions (TFD)
- Algorithms to compute quadratic TFDs.
- Saves computation and computer memory, thus enabling computation of TFDs for
long-duration signals.
- code (recommend): [github | Matlab code](https://github.com/otoolej/memeff_TFDs)
- code (for exact TFD): [github | Matlab code](https://github.com/otoolej/fast_TFDs)
- paper: [O'Toole and Boashash, App Comp Harm Anal, 2013](https://doi.org/10.1016/j.acha.2013.01.003)
- book chaper: JM O'Toole and B Boashash, “Memory Efficient Algorithms for Quadratic
  TFDs”, Chapter 6.6; in Time–Frequency Signal Processing and Analysis: A Comprenhensive
  Reference, Second Edition, Academic Press, pp. 374–385, 2016 (ISBN: 9780123984999).


## Methods to Estimate the Instantaneous Frequency from TFDs
- Two methods to extract/estimate the Instantaneous Frequency (IF) from TFDs.
- Method 1 uses an edge-linking strategy (see [Rankine et al.,
  2007](https://doi.org/10.1016/j.sigpro.2006.10.013)); Methods 2 uses the concept of
  finite duration IF components [McAulay and Quatieri,
  1986](https://doi.org/10.1109/TASSP.1986.1164910)
- code: [github | Matlab code](https://github.com/otoolej/time_frequency_tracks)
- papers: [Rankine et al., 2007](https://doi.org/10.1016/j.sigpro.2006.10.013) and
  [McAulay and Quatieri, 1986](https://doi.org/10.1109/TASSP.1986.1164910); also see list
  of references in [github page](https://github.com/otoolej/time_frequency_tracks#references).

___

# Tools for Connectivity
## Features of Nonstationary Directional Coupling
- Code to generate a short-time information partial directed coherence (ST-iPDC) function
  and code to extract nonstationary and time-varying directional features from the ST-iPDC.
- Also includes a 2D fractal dimension measure.
- code: [github | Matlab code](https://github.com/otoolej/nonstat_directional_coupling)
- paper: [O'Toole et al., Physiological Measurement, 2021](https://doi.org/10.1088/1361-6579/abe3de)

___

# Signal-Processing and Machine-learning Tools
## Random Convolution Kernels with Multiscale Decomposition
- Zero-knowledge machine-learning algorithm.
- Adapted from [ROCKET](https://github.com/angus924/rocket) to incorporate multiscale analysis.
- code: [github | Python code](https://github.com/otoolej/ms_rocket)
- paper: [Lundy and O'Toole, EUSIPCO-2021](https://doi.org/10.23919/EUSIPCO54536.2021.9616281)


## Mutual information estimates
- Fast implementation of methods for calculating mutual information, for both the
  continuous--continuous case and discrete--continuous case.
- code: [github | Matlab code](https://github.com/otoolej/mutual_info_kNN)
- paper: [Kraskov et al., 2004](https://doi.org/10.1103/PhysRevE.69.066138) and [Ross 2014](https://doi.org/10.1371/journal.pone.0087357).


## Envelope--Derivative Operator
- A frequency-weighted energy operator (also used as burst-detector).
- code: [github | Matlab version](https://github.com/otoolej/nonlinear-energy-operators)
- code: [github | Python version](https://github.com/otoolej/envelope_derivative_operator)
- paper: [O'Toole et al., EMBC-2014](https://doi.org/10.1109/EMBC.2014.6944325)

---

# Code to Accompany Published Papers

## Plots for Review Paper on Time--Frequency Processing of Nonstationary Biomedical signals
- Plot of time--frequency analysis methods in review paper for IEEE Signal Processing Magazine.
- code: [github | Matlab code](https://github.com/otoolej/plot_TFDs_SPmag_paper)
- paper: [Boashash et al., 2013](https://doi.org/10.1109/MSP.2013.2265914)


## Monitoring cerebral oxygenation of preterm infants using a neonatal specific sensor
- Methods for determining association with short-term clinical outcome (brain injury or
death) and cerebral oxygenation as measured by NIRS.
- code: [github | R and Matlab code](https://github.com/otoolej/rcSO2_temp_evolution)
- paper: [DOI: 10.1038/s41372-017-0007-5](https://doi.org/10.1038/s41372-017-0007-5)


## Quantitative features of the EEG recorded minutes after birth
- Quantitative analysis of EEG recorded in the delivery room.
- code: [github | Matlab code](https://github.com/otoolej/delivery_room_qEEG)
- paper: [DOI: 10.1136/archdischild-2018-315231](https://doi.org/10.1136/archdischild-2018-315231)


## Evolution of qEEG in preterm infants over the first days of life
- Methods to track the evolution of the EEG over the first 3 days after birth.
- code: [github | R and Matlab code](https://github.com/otoolej/postnatal_EEG_evolution)
- paper: [DOI: 10.1038/s41598-019-41227-9](https://doi.org/10.1038/s41598-019-41227-9)

## EEG concordance in preterm twins
- Methods to compare qEEG features between preterm singletons and twins.
- code: [github | R and Matlab code](https://github.com/otoolej/preterm_twins_EEG)
- paper: [Lloyd et al., J Clin Neurphys, 2021](https://doi.org/10.1097/WNP.0000000000000645)


---
This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).


