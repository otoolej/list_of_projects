List of repositories. Neonatal EEG algorithms and some generic signal processing tools


# Quantitative EEG (qEEG)
## NEURAL -- a neonatal EEG feature set in Matlab
- [github (Matlab version)](https://github.com/otoolej/qEEG_feature_set)
- [github (Python version)](https://github.com/BrianMur92/NEURAL_py_EEG_feature_set)


# Detecting Bursts or Inter-Bursts in Neonatal EEG

## Inter-Burst Detector 
### Preterm EEG 
#### Method: features + SVM
- [github | Python version](https://github.com/otoolej/py_burst_detector)
- [github | Matlab version](https://github.com/otoolej/burst_detector)

#### Method: single feature 
- generic method to detect bursts: high-amplitude coupled with high-frequency 
- Includes envelope derivative operator (EDO) and nonlinear energy operator (NLEO)
- [github | Matlab version](https://github.com/otoolej/nonlinear-energy-operators)
- [github | Python version](https://github.com/otoolej/envelope_derivative_operator)


### Term EEG (in trace alternant activity)
- [github | Matlab code](https://github.com/sumitraurale/interburst_detector)


## Burst Detector 
### Preterm EEG
- method to detect short-duration bursts of activity in preterm (<32 weeks GA) EEG
- [github | Python code](https://github.com/BrianMur92/Preterm_transient_burst_detector)


# Tools for Time--Frequency Signal Analysis

## Fast and Memory Efficient Algorithms for Computing Time--Frequency Distributions (TFD)
- recommend: [github | Matlab code](https://github.com/otoolej/memeff_TFDs)
- if want exact TFD: [github | Matlab code](https://github.com/otoolej/fast_TFDs)

## Methods to Estimate the Instantaneous Frequency from TFDs
- [github | Matlab code](https://github.com/otoolej/time_frequency_tracks)


# Tools for Connectivity
## Features of Nonstationary Directional Coupling
- [github | Matlab code](https://github.com/otoolej/nonstat_directional_coupling)
- (includes modified 2D fractal dimension measure)


# Signal-Processing Tools
## Mutual information estimates
- [github | Matlab code](https://github.com/otoolej/mutual_info_kNN)
- fast implementation of methods for calculating mutual information (for both the
  continuous--continuous case and discrete--continuous case)

## Envelope--Derivative Operator
- A frequency-weighted energy operator (also used as burst-detector in above)
- [github | Matlab version](https://github.com/otoolej/nonlinear-energy-operators)
- [github | Python version](https://github.com/otoolej/envelope_derivative_operator)



# Code to Accompany Published Papers
## Monitoring cerebral oxygenation of preterm infants using a neonatal specific sensor
- [github | R and Matlab code](https://github.com/otoolej/rcSO2_temp_evolution)
- paper: [DOI: 10.1038/s41372-017-0007-5](https://doi.org/10.1038/s41372-017-0007-5)


## Quantitative features of the EEG recorded minutes after birth
- [github | Matlab code](https://github.com/otoolej/delivery_room_qEEG)
- paper: [DOI: 10.1136/archdischild-2018-315231](https://doi.org/10.1136/archdischild-2018-315231)


## Evolution of qEEG in preterm infants over the first days of life
- [github | R and Matlab code](https://github.com/otoolej/postnatal_EEG_evolution)
- paper: [DOI: 10.1038/s41598-019-41227-9](https://doi.org/10.1038/s41598-019-41227-9)

