# Cantilever Beam Vibration Project

An experimental vibration analysis project investigating how added mass affects the dynamic response of a cantilever beam using an accelerometer, National Instruments DAQ hardware, and LabVIEW.

## Project Overview

The objective of this project was to measure the free-vibration response of a cantilever beam and determine how its oscillation period and frequency changed as additional mass was added.

The beam was excited manually and allowed to vibrate freely while an accelerometer measured its motion. The sensor output was recorded as voltage versus time through an **NI USB-6341 DAQ** and a custom **LabVIEW** data-acquisition setup.

Tests were performed with **no added mass, 1 lb, 3 lb, and 5 lb**. The time between consecutive oscillation peaks was used to estimate the vibration period, and the corresponding frequency was calculated for each loading condition.

## Key Features

- **Experimental Vibration Measurement:** Captured cantilever beam motion using an accelerometer and NI data-acquisition hardware.

- **LabVIEW Data Acquisition:** Developed a LabVIEW VI to display the live waveform and save each experimental trial for analysis.

- **High-Rate Sampling:** Recorded vibration signals at a **1000 Hz sampling rate** for accurate identification of oscillation peaks.

- **Peak-Based Frequency Analysis:** Estimated oscillation period from consecutive peaks and calculated frequency using `f = 1/T`.

- **Mass-Loading Comparison:** Evaluated beam response under **0, 1, 3, and 5 lb** loading conditions.

## Experimental Setup

The system consisted of:

- Metal cantilever beam
- Accelerometer mounted near the free end
- **National Instruments USB-6341 DAQ**
- **LabVIEW**
- 3.3 V power supply
- Added masses of **1 lb, 3 lb, and 5 lb**

The accelerometer converted beam motion into a voltage signal, which was acquired by the DAQ and recorded in LabVIEW as a time-dependent waveform.

## Data Acquisition & Analysis

Each test followed the same general procedure:

1. Mount the accelerometer and selected mass to the beam.
2. Confirm a stable accelerometer signal in LabVIEW.
3. Excite the beam and allow it to vibrate freely.
4. Record the voltage response at a **0.001 s sampling interval**.
5. Identify consecutive vibration peaks.
6. Estimate the average period and calculate the corresponding frequency.

## Results

Increasing the attached mass produced a clear decrease in vibration frequency and an increase in oscillation period.

| Added Mass | Period (s) | Frequency (Hz) |
|---|---:|---:|
| 0 lb | 0.099 | 10.13 |
| 1 lb | 0.118 | 8.48 |
| 3 lb | 0.140 | 7.14 |
| 5 lb | 0.169 | 5.92 |

The measured frequency decreased from approximately **10.13 Hz with no added mass to 5.92 Hz with 5 lb**, while the period increased from approximately **0.099 s to 0.169 s**.

These results demonstrate that increasing the effective mass of the cantilever system causes it to oscillate more slowly, consistent with expected vibration behavior.

## Engineering Application

Understanding how added mass changes structural vibration is important when predicting **natural frequencies and avoiding resonance** in engineering systems. Similar effects occur in structures such as aircraft wings, bridges, and other components whose vibration behavior changes as payload or structural mass is added.

## Limitations

The recorded signals contained some electrical noise and occasional spikes, and the beam was manually excited, causing differences in initial amplitude between trials.

Because the frequencies were estimated from measured waveform peaks, the reported values should be interpreted as experimental estimates rather than exact theoretical natural frequencies.

## Technologies & Equipment

- **Data Acquisition:** LabVIEW
- **DAQ Hardware:** NI USB-6341
- **Sensor:** Accelerometer
- **Sampling Rate:** 1000 Hz
- **Analysis:** Time-domain peak detection and frequency estimation
- **Experimental Mechanics:** Cantilever beam free-vibration testing

## Project Documentation

📄 [View Project Presentation](Cantilever_Beam_Vibration_Project.pdf)

The full presentation includes the experimental setup, LabVIEW VI, recorded waveforms, peak analysis, results, and discussion.
