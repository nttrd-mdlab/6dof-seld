# 6DoF SELD
6DoF SELD is the sound event localization and detection (SELD) task using wearable equipment for a moving human, such as a pedestrian. 
This repository provides description of a published dataset designed for this task and source code of our proposed method[to be appeared].
![overview-1](https://github.com/nttrd-mdlab/6dof-seld/assets/72438001/205e4488-2681-42cd-8e13-54cf83544618)


## 6DoF SELD Dataset
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10473531.svg)](https://doi.org/10.5281/zenodo.10473531)
### Dataset overview
The 6DoF SELD Dataset is a SELD dataset for detecting and localizing sound events from the view of self-motion humans. Unlike conventional SELD datasets using fixed microphone arrays or wearable SELD datasets using HATS, sound events are recorded by a headphone-type device worn by a subject performing 6DoF self-motion (walking and looking around). The headphone-type device is equipped with an 18-channel microphone array and three motion tracking sensors. The motion tracking sensors allow the head's position and posture to be observed. The position and posture acquired by the motion tracking sensors can be time differentiated to simulate the observation of head motion by more practical sensors, such as a 6-axis inertial measurement unit (IMU).

### Folder Structure 

### Recording details
The following figure shows the recording setup and equipment configuration for the 6DoF SELD Dataset. 
![setup-1](https://github.com/nttrd-mdlab/6dof-seld/assets/72438001/441bda8b-2018-4f9e-997c-a1e886348db9)

The recording was conducted in the room with variable reverberation, as shown in (a). A person wearing a headphone-type device moves in the red-circled area, and sound events are randomly played back in the blue-circled area. The (b) shows the details of the headphone-type device. 8-channel microphones are attached to the outer edges of the plastic earpads on the left and right sides, and a single-channel microphone is attached in the center. Three motion trackers are attached to the headband. The position and posture of the head are observed as the center of gravity and posture of the triangle composed by these three motion trackers. The sound event generation system is shown in (c). Sound events are generated by randomly playing sound clips from two speakers. The speakers are manually moved to various heights and angles to reproduce changes in the direction of the arrival of sound events. The position of the sound event is recorded in the absolute coordinate system of the room by the motion tracking sensor and transformed into a coordinate system relative to the head of the central figure based on the observed head posture information.

The following table shows the specifications of the 6DoF SELD dataset and the conventional SELD dataset.

| Dataset           | Amount of data | Self-motion of mic. |  Subjects | SOurse movement | # of classes | # of  mic. | SNR [dB] | Rooms |
|-------------------|----------------|:-------------------:|:---------:|:---------------:|:------------:|:----------:|:--------:|:-----:|
| 6DoF SELD Dataset | 20.1h          |   stat./3DoF/6DoF   | 3 (Human) |      Fixed      |      12      |     18     |  6 - 20  |   3   |

The dataset is divided into three subsets ("stat.", "3DoF", and "6DoF") according to the state of self-motion: in "stat." the subject remains seated in a chair; in "3DoF" the subject performs head and body rotation movements while standing, and in "6DoF" the subject performs a 0.5 m rotation movement. They walk, change direction, and turn in a circle of 75 m. In "6DoF," subjects walk, change direction, and turn in a circle of 75 m. The signal-to-noise ratio (SNR) was controlled to 6, 10, and 20 dB. The recording room is equipped with a variable reverberation chamber, with reverberation time controlled in three steps ($T_{60}^{500Hz} = 0.12, 0.30, 0.41$ sec).

All microphones used for recording were Hosiden KUB4225 with a sampling frequency of 48k and a bit depth of 16 bits; the motion tracking sensor was a combination of HTC Vive Tracker (2018) and HTC SteamVR Base Station 2.0. Sensor signals were recorded at a non-uniform sampling rate of approximately 40 fps and then downsampled to a uniform sampling rate of 20 fps.

## Citation
M. Yasuda, S. Saito, A. Nakayama, and N. Harada, "6DoF SELD : SOUND EVENT LOCALIZATION AND DETECTION USING MICROPHONES AND MOTION TRACKING SENSORS ON SELF-MOTIONING HUMAN", ICASSP2024 (accepted).

## Contact
masahiro.yasuda@ntt.com (Masahiro Yasuda)
